---
sidebar_position: 3
---

# Executing a route

Once you have decided on a suitable route to execute. You may start engaging the sdk to execute it.

For the simplest way to execute routes, you can [connect a web3 provider](./web3-provider-execute.md). This will take care of most of the execution process.

For the more controlled process, read on.

It's important to first understand what is required to execute a trade.

## Requirements

1. Have a user address to execute the trade with
2. Be able to prompt the user for transactions (such as using `ethers.js`)
3. Be able to use rpc providers configured to the requested chain when required by the sdk.

## Execution process

1. You start the trade and pull the next transaction to execute
2. The transaction may require an approval, for example when ERC20 tokens are involved. Check if approval is required and execute it using the provided transaction data.
3. Retrieve the transaction data for the current transaction and execute it.
4. Submit the transaction hash while pulling the next transaction to execute.

## Pulling transactions

Assuming you have already [Selected a route](./query-routes.md#querying-the-best-route) to execute

You must first start the quote and retrieve it's generator:

```ts
const execute = await socket.start(quote);
```

Next you can pull the transactions until they complete using a while loop. Remember to submit the transaction that you executed when retrieving the next transaction.

```ts
let next = await execute.next();
while (!next.done && next.value) {
  const tx = next.value;
  next = await execute.next("0x000"); // <- The transaction hash of the current transaction
}
```

For each transaction, you must first check whether it requires an approval. If it does, execute that transaction.

```ts
const approvalTxData = await tx.getApproveTransaction();
if (approvalTxData) {
  const approvalTx = await wallet.sendTransaction(approvalTxData);
  await approvalTx.wait();
}
```

If you require to know the chain that this transaction needs to be sent on, it is available at `tx.chainId`.

Next, retrieve the send transaction and send it:

```ts
const sendTxData = await tx.getSendTransaction();
const sendTx = await wallet.sendTransaction(sendTxData);
await sendTx.wait();
```

Submit the transaction hash to proceed to the next step:

```ts
next = await execute.next(sendTx.hash);
```

## Full Code

Finally, it will look something like the following:

```ts
const quote = await socket.getBestQuote({ path, amount, address });
const execute = await socket.start(quote);

while (!next.done && next.value) {
  const tx = next.value;
  // Setup the provider and wallet based on `tx.chainId` and `quote.sender` if needed
  const approvalTxData = await tx.getApproveTransaction();
  if (approvalTxData) {
    const approvalTx = await wallet
      .connect(provider)
      .sendTransaction(approvalTxData);
    await approvalTx.wait();
  }
  const sendTxData = await tx.getSendTransaction();
  const sendTx = await wallet.connect(provider).sendTransaction(sendTxData);
  await sendTx.wait();
  next = await execute.next(sendTx.hash);
}
```

---
sidebar_position: 2
---

# Query Routes

In order to execute trades using socket, we must first establish the tokens being exchanged and the path.

## Initialise the SDK

First initialise the SDK with an api key. By default the sdk will return both single and multi-transaction routes.

```ts
const socket = new Socket({ apiKey: API_KEY });
```

If you would like to only receive single transaction routes, set `singleTxOnly: true`

```ts
const socket = new Socket({
  apiKey: API_KEY
  defaultQuotePreferences: {
    singleTxOnly: true,
  }
});

```

## Retreiving the available tokens

There are a defined set of tokens that can be traded using the socket protocol for a given `from` and `to` chain. You can retrieve a list of these tokens:

```ts
const tokenList = await socket.getTokenList({
  fromChainId: ChainId.MAINNET_CHAIN_ID, // Ethereum Mainnet
  toChainId: ChainId.POLYGON_CHAIN_ID, // Polygon Mainnet
});
```

The list of tokens for each chain can be accessed as such:

```ts
tokenList.from; // Tokens on the from chain
tokenList.to; // Tokens on the to chain
```

There are utilities for retrieving tokens:

```ts
const eth = tokenList.from.nativeToken;
const matic =
  tokenList.to.tokenByAddress(0xeeeeeeeeeeeeeeeeeeeeeeeeeeeeeeeeeeeeeeee);
```

## Creating a path

Now we are ready to create a path which trades a `fromToken` to the destination `toToken`.

```ts
const path = new Path({ fromToken: eth, toToken: matic });
```

## Querying the best route

Input the path, the amount to trade and the user's address in order to retrieve a quote.

```ts
const quote = await socket.getBestQuote({
  path,
  amount: "1000000000000000000", // 1 ETH
  address: "<USER_ADDRESS_HERE",
});
```

You can also retrieve the full list of quotes from the api using `socket.getAllRoutes`.

If you would like to further customize the quotes that are returned, pass a [`QuotePreferences`](../reference/interfaces/QuotePreferences.md) object to the quote call. For example:

```ts
const fastestQuote = await socket.getBestQuote(
  {
    path,
    amount,
    address,
  },
  { sort: "time" }
);
```

You are now ready to execute the quote. You may do this by [connecting a wallet with Web3Providers](../guides/web3-provider-execute.md) or [manually](../guides/execute-routes.md).

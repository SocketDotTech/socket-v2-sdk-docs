---
sidebar_position: 4
---

# Executing with Web3 Provider

The easiest way to execute routes using the Socket SDK is by connecting a web3 provider. Using this method, the SDK will handle the entire process of the transaction, including approvals, prompting wallets, switching networks and more.

The SDK supports the [ethers Web3Provider](https://docs.ethers.io/v5/api/providers/other/#Web3Provider). Many wallet libraries like [`web3modal`](https://github.com/WalletConnect/web3modal) and [`web3onboard`](https://docs.blocknative.com/onboard) support retrieving the web3 provider for the connected wallet.

## Connecting

Using the constructed socket instance, call `connect` with the web3 provider. Web3Modal is being used as example here but any web3 provider can be used.

```ts
const web3ModalProvider = await web3Modal.connect();
const web3Provider = new ethers.providers.Web3Provider(
  web3ModalProvider,
  "any"
);
const socket = new Socket({ apiKey: API_KEY });
const web3Socket = socket.connect(web3Provider);
```

## Executing

To begin the execution simply call start:

```ts
const activeRouteId = await web3Socket.start(quote);
```

## Events

In order to follow the execution process, you may specify [EventCallbacks](../reference/interfaces/EventCallbacks.md) that will be called during the process.

```ts
await web3Socket.start(quote, {
  onDone: (activeRouteId) => {
    console.log("Executing route complete", tx);
  },
});
```

Most callbacks can also return a callback that will be called when the action has been completed. For example, you can detect when an approval transaction is complete:

```ts
await web3Socket.start(quote, {
  onApprove: (tx) => {
    console.log("Requesting approval");
    return (tx, hash) => {
      console.log("Approval complete", hash);
    };
  },
});
```

For a complete list of callbacks see [EventCallbacks](../reference/interfaces/EventCallbacks.md).

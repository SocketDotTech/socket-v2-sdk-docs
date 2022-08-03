---
sidebar_position: 5
---

# Continue a route

In certain circumstances, you may be required to continue a route that was started.

You will need the `activeRouteId` for the route to continue.

When starting a route using `socket.start(...)` the `activeRouteId` is returned. In the case that it is no longer available, there are ways to find it.

## Finding the active route ID

[`getActiveRoutes`](../reference/sdk/Socket#getactiveroutes) can be used to find active routes.

For example to retrieve by the user address:

```ts
const activeRoutes = socket.getActiveRoutes({
  userAddress: "0xd8da6bf26964af9d7eed9e03e53415d37aa96045",
});

const route = activeRoutes.find(
  (route) => route.fromChainId === ChainId.MAINNET_CHAIN_ID
);

console.log(route.activeRouteId);
```

## Continuing the route

Call `socket.continue` with the `activeRouteId`. The process is continued with the same interface as `socket.start`.

```ts
await socket.continue(activeRouteId);
...
```

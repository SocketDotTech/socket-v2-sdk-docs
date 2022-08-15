# Routes

## Table of contents

### Constructors

- [constructor](Routes.md#constructor)

### Methods

- [getActiveRoute](Routes.md#getactiveroute)
- [getActiveRoutesForUser](Routes.md#getactiveroutesforuser)
- [nextTx](Routes.md#nexttx)
- [startActiveRoute](Routes.md#startactiveroute)
- [updateActiveRoute](Routes.md#updateactiveroute)

## Constructors

### constructor

• **new Routes**()

## Methods

### getActiveRoute

▸ `Static` **getActiveRoute**(`__namedParameters`): [`CancelablePromise`](../client/CancelablePromise.md)<[`ActiveRouteOutputDTO`](../types.md#activerouteoutputdto)\>

**`throws`** ApiError

#### Parameters

| Name                              | Type     | Description             |
| :-------------------------------- | :------- | :---------------------- |
| `__namedParameters`               | `Object` | -                       |
| `__namedParameters.activeRouteId` | `number` | Id of the Active Route. |

#### Returns

[`CancelablePromise`](../client/CancelablePromise.md)<[`ActiveRouteOutputDTO`](../types.md#activerouteoutputdto)\>

ActiveRouteDTO Get active route details using active route id

#### Defined in

[socket-v2-sdk/src/client/services/Routes.ts:43](https://github.com/SocketDotTech/socket-v2-sdk/blob/91d9fe3/src/client/services/Routes.ts#L43)

---

### getActiveRoutesForUser

▸ `Static` **getActiveRoutesForUser**(`request`): [`CancelablePromise`](../client/CancelablePromise.md)<[`ActiveRoutesOutputDTO`](../types.md#activeroutesoutputdto)\>

**`throws`** ApiError

#### Parameters

| Name      | Type                                                          |
| :-------- | :------------------------------------------------------------ |
| `request` | [`ActiveRoutesRequest`](../interfaces/ActiveRoutesRequest.md) |

#### Returns

[`CancelablePromise`](../client/CancelablePromise.md)<[`ActiveRoutesOutputDTO`](../types.md#activeroutesoutputdto)\>

ActiveRoutesOutputDTO Get all the active routes from a user address. Filters like fromChainId, toChainId and token addresses can be used to get back specific active routes.

#### Defined in

[socket-v2-sdk/src/client/services/Routes.ts:65](https://github.com/SocketDotTech/socket-v2-sdk/blob/91d9fe3/src/client/services/Routes.ts#L65)

---

### nextTx

▸ `Static` **nextTx**(`__namedParameters`): [`CancelablePromise`](../client/CancelablePromise.md)<[`NextTxOutputDTO`](../types.md#nexttxoutputdto)\>

**`throws`** ApiError

#### Parameters

| Name                              | Type     | Description         |
| :-------------------------------- | :------- | :------------------ |
| `__namedParameters`               | `Object` | -                   |
| `__namedParameters.activeRouteId` | `number` | Id of Active Route. |

#### Returns

[`CancelablePromise`](../client/CancelablePromise.md)<[`NextTxOutputDTO`](../types.md#nexttxoutputdto)\>

NextTxOutputDTO Get next tx details of an active route

#### Defined in

[socket-v2-sdk/src/client/services/Routes.ts:82](https://github.com/SocketDotTech/socket-v2-sdk/blob/91d9fe3/src/client/services/Routes.ts#L82)

---

### startActiveRoute

▸ `Static` **startActiveRoute**(`__namedParameters`): [`CancelablePromise`](../client/CancelablePromise.md)<[`NextTxOutputDTO`](../types.md#nexttxoutputdto)\>

Function that takes in a route and starts the selected route.
Function is responsible for

- Saving the selected route to bridge tokens from one chain to another.
- Saving the fromChain, toChain, and fromAsssetAddress and toAssetAddress
- Returns the Active Route Id, Current Tx, Total number of txs, txType

**`throws`** ApiError

#### Parameters

| Name                             | Type                                                               |
| :------------------------------- | :----------------------------------------------------------------- |
| `__namedParameters`              | `Object`                                                           |
| `__namedParameters.startRequest` | [`StartActiveRouteInputDTO`](../types.md#startactiverouteinputdto) |

#### Returns

[`CancelablePromise`](../client/CancelablePromise.md)<[`NextTxOutputDTO`](../types.md#nexttxoutputdto)\>

StartActiveRouteResponseDTO Starts the Active Route and gives back the data to start the route

#### Defined in

[socket-v2-sdk/src/client/services/Routes.ts:23](https://github.com/SocketDotTech/socket-v2-sdk/blob/91d9fe3/src/client/services/Routes.ts#L23)

---

### updateActiveRoute

▸ `Static` **updateActiveRoute**(`__namedParameters`): [`CancelablePromise`](../client/CancelablePromise.md)<[`RouteStatusOutputDTO`](../types.md#routestatusoutputdto)\>

**`throws`** ApiError

#### Parameters

| Name                              | Type     | Description                                                                                                                                                                                                                             |
| :-------------------------------- | :------- | :-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| `__namedParameters`               | `Object` | -                                                                                                                                                                                                                                       |
| `__namedParameters.activeRouteId` | `number` | Id of Active Route.                                                                                                                                                                                                                     |
| `__namedParameters.signature?`    | `string` | Signature to be sent in case the next transaction is dependant on the signature.                                                                                                                                                        |
| `__namedParameters.txHash?`       | `string` | Transaction hash that relates to the userTxIndex. Each object in the userTxs is a transaction that has to be done by the user to progress in the route. If all the transactions are completed in the route, it will be marked complete. |
| `__namedParameters.userTxIndex`   | `number` | Index of the userTxs in the Active Route. Every active route will have a userTxs array. userTxIndex is the index of the object in the userTxs array.                                                                                    |

#### Returns

[`CancelablePromise`](../client/CancelablePromise.md)<[`RouteStatusOutputDTO`](../types.md#routestatusoutputdto)\>

RouteStatusOutputDTO Get status of an active route while submitting transaction

#### Defined in

[socket-v2-sdk/src/client/services/Routes.ts:104](https://github.com/SocketDotTech/socket-v2-sdk/blob/91d9fe3/src/client/services/Routes.ts#L104)

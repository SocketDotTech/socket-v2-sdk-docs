# EventCallbacks

## Table of contents

### Methods

- [onApprove](EventCallbacks.md#onapprove)
- [onChainSwitch](EventCallbacks.md#onchainswitch)
- [onDone](EventCallbacks.md#ondone)
- [onSend](EventCallbacks.md#onsend)
- [onTx](EventCallbacks.md#ontx)

## Methods

### onApprove

▸ `Optional` **onApprove**(`tx`): `void` \| [`TxDoneCallback`](../types.md#txdonecallback)

Callback when an approval is being requested.

#### Parameters

| Name | Type                             |
| :--- | :------------------------------- |
| `tx` | [`SocketTx`](../sdk/SocketTx.md) |

#### Returns

`void` \| [`TxDoneCallback`](../types.md#txdonecallback)

#### Defined in

[socket-v2-sdk/src/web3ConnectedSocket.ts:32](https://github.com/rugamoto/socket-v2-sdk/blob/b3c3e8d/src/web3ConnectedSocket.ts#L32)

---

### onChainSwitch

▸ `Optional` **onChainSwitch**(`fromChainId`, `toChainId`): `void` \| [`ChainSwitchDoneCallback`](../types.md#chainswitchdonecallback)

Callback when switching chains is being requested.

#### Parameters

| Name          | Type                             |
| :------------ | :------------------------------- |
| `fromChainId` | [`ChainId`](../enums/ChainId.md) |
| `toChainId`   | [`ChainId`](../enums/ChainId.md) |

#### Returns

`void` \| [`ChainSwitchDoneCallback`](../types.md#chainswitchdonecallback)

#### Defined in

[socket-v2-sdk/src/web3ConnectedSocket.ts:36](https://github.com/rugamoto/socket-v2-sdk/blob/b3c3e8d/src/web3ConnectedSocket.ts#L36)

---

### onDone

▸ `Optional` **onDone**(`activerouteId`): `void`

Callback when the route execution has completed.

#### Parameters

| Name            | Type     |
| :-------------- | :------- |
| `activerouteId` | `number` |

#### Returns

`void`

#### Defined in

[socket-v2-sdk/src/web3ConnectedSocket.ts:38](https://github.com/rugamoto/socket-v2-sdk/blob/b3c3e8d/src/web3ConnectedSocket.ts#L38)

---

### onSend

▸ `Optional` **onSend**(`tx`): `void` \| [`TxDoneCallback`](../types.md#txdonecallback)

Callback when a send transaction is being requested.

#### Parameters

| Name | Type                             |
| :--- | :------------------------------- |
| `tx` | [`SocketTx`](../sdk/SocketTx.md) |

#### Returns

`void` \| [`TxDoneCallback`](../types.md#txdonecallback)

#### Defined in

[socket-v2-sdk/src/web3ConnectedSocket.ts:34](https://github.com/rugamoto/socket-v2-sdk/blob/b3c3e8d/src/web3ConnectedSocket.ts#L34)

---

### onTx

▸ `Optional` **onTx**(`tx`): `void` \| [`SocketTxDoneCallback`](../types.md#sockettxdonecallback)

Callback when a new socket transaction has begun.

#### Parameters

| Name | Type                             |
| :--- | :------------------------------- |
| `tx` | [`SocketTx`](../sdk/SocketTx.md) |

#### Returns

`void` \| [`SocketTxDoneCallback`](../types.md#sockettxdonecallback)

#### Defined in

[socket-v2-sdk/src/web3ConnectedSocket.ts:30](https://github.com/rugamoto/socket-v2-sdk/blob/b3c3e8d/src/web3ConnectedSocket.ts#L30)

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

#### Parameters

| Name | Type                             |
| :--- | :------------------------------- |
| `tx` | [`SocketTx`](../sdk/SocketTx.md) |

#### Returns

`void` \| [`TxDoneCallback`](../types.md#txdonecallback)

#### Defined in

[socket-v2-sdk/src/web3ConnectedSocket.ts:27](https://github.com/rugamoto/socket-v2-sdk/blob/91d9fe3/src/web3ConnectedSocket.ts#L27)

---

### onChainSwitch

▸ `Optional` **onChainSwitch**(`fromChainId`, `toChainId`): `void` \| [`ChainSwitchDoneCallback`](../types.md#chainswitchdonecallback)

#### Parameters

| Name          | Type                             |
| :------------ | :------------------------------- |
| `fromChainId` | [`ChainId`](../enums/ChainId.md) |
| `toChainId`   | [`ChainId`](../enums/ChainId.md) |

#### Returns

`void` \| [`ChainSwitchDoneCallback`](../types.md#chainswitchdonecallback)

#### Defined in

[socket-v2-sdk/src/web3ConnectedSocket.ts:29](https://github.com/rugamoto/socket-v2-sdk/blob/91d9fe3/src/web3ConnectedSocket.ts#L29)

---

### onDone

▸ `Optional` **onDone**(`activerouteId`): `void`

#### Parameters

| Name            | Type     |
| :-------------- | :------- |
| `activerouteId` | `number` |

#### Returns

`void`

#### Defined in

[socket-v2-sdk/src/web3ConnectedSocket.ts:30](https://github.com/rugamoto/socket-v2-sdk/blob/91d9fe3/src/web3ConnectedSocket.ts#L30)

---

### onSend

▸ `Optional` **onSend**(`tx`): `void` \| [`TxDoneCallback`](../types.md#txdonecallback)

#### Parameters

| Name | Type                             |
| :--- | :------------------------------- |
| `tx` | [`SocketTx`](../sdk/SocketTx.md) |

#### Returns

`void` \| [`TxDoneCallback`](../types.md#txdonecallback)

#### Defined in

[socket-v2-sdk/src/web3ConnectedSocket.ts:28](https://github.com/rugamoto/socket-v2-sdk/blob/91d9fe3/src/web3ConnectedSocket.ts#L28)

---

### onTx

▸ `Optional` **onTx**(`tx`): `void` \| [`SocketTxDoneCallback`](../types.md#sockettxdonecallback)

#### Parameters

| Name | Type                             |
| :--- | :------------------------------- |
| `tx` | [`SocketTx`](../sdk/SocketTx.md) |

#### Returns

`void` \| [`SocketTxDoneCallback`](../types.md#sockettxdonecallback)

#### Defined in

[socket-v2-sdk/src/web3ConnectedSocket.ts:26](https://github.com/rugamoto/socket-v2-sdk/blob/91d9fe3/src/web3ConnectedSocket.ts#L26)

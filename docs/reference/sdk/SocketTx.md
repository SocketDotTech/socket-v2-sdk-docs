# SocketTx

An entity representing the transaction prompted by the socket api

## Hierarchy

- [`NextTxResponse`](../interfaces/NextTxResponse.md)

  ↳ **`SocketTx`**

## Table of contents

### Constructors

- [constructor](SocketTx.md#constructor)

### Properties

- [activeRouteId](SocketTx.md#activerouteid)
- [approvalChecked](SocketTx.md#approvalchecked)
- [approvalData](SocketTx.md#approvaldata)
- [chainId](SocketTx.md#chainid)
- [done](SocketTx.md#done)
- [hash](SocketTx.md#hash)
- [totalUserTx](SocketTx.md#totalusertx)
- [txData](SocketTx.md#txdata)
- [txTarget](SocketTx.md#txtarget)
- [txType](SocketTx.md#txtype)
- [userTxIndex](SocketTx.md#usertxindex)
- [userTxType](SocketTx.md#usertxtype)
- [value](SocketTx.md#value)

### Methods

- [approvalRequired](SocketTx.md#approvalrequired)
- [getApproveTransaction](SocketTx.md#getapprovetransaction)
- [getSendTransaction](SocketTx.md#getsendtransaction)
- [submit](SocketTx.md#submit)

## Constructors

### constructor

• **new SocketTx**(`nextTx`, `statusCheckInterval?`)

#### Parameters

| Name                  | Type                                                | Default value | Description                                                              |
| :-------------------- | :-------------------------------------------------- | :------------ | :----------------------------------------------------------------------- |
| `nextTx`              | [`NextTxResponse`](../interfaces/NextTxResponse.md) | `undefined`   | The api object for the next transaction                                  |
| `statusCheckInterval` | `number`                                            | `10000`       | How often in ms to poll for status updates when checking the transaction |

#### Inherited from

NextTxResponse.constructor

#### Defined in

[socket-v2-sdk/src/socketTx.ts:36](https://github.com/rugamoto/socket-v2-sdk/blob/b3c3e8d/src/socketTx.ts#L36)

## Properties

### activeRouteId

• **activeRouteId**: `number`

Id of Active Route.

#### Inherited from

[NextTxResponse](../interfaces/NextTxResponse.md).[activeRouteId](../interfaces/NextTxResponse.md#activerouteid)

#### Defined in

[socket-v2-sdk/src/client/models/NextTxResponse.ts:10](https://github.com/rugamoto/socket-v2-sdk/blob/b3c3e8d/src/client/models/NextTxResponse.ts#L10)

---

### approvalChecked

• **approvalChecked**: `boolean` = `false`

If the approval has been checked

#### Defined in

[socket-v2-sdk/src/socketTx.ts:22](https://github.com/rugamoto/socket-v2-sdk/blob/b3c3e8d/src/socketTx.ts#L22)

---

### approvalData

• **approvalData**: `null` \| [`ApprovalData`](../types.md#approvaldata)

#### Inherited from

[NextTxResponse](../interfaces/NextTxResponse.md).[approvalData](../interfaces/NextTxResponse.md#approvaldata)

#### Defined in

[socket-v2-sdk/src/client/models/NextTxResponse.ts:44](https://github.com/rugamoto/socket-v2-sdk/blob/b3c3e8d/src/client/models/NextTxResponse.ts#L44)

---

### chainId

• **chainId**: [`ChainId`](../enums/ChainId.md)

Id of chain where transaction has to be sent.

#### Inherited from

[NextTxResponse](../interfaces/NextTxResponse.md).[chainId](../interfaces/NextTxResponse.md#chainid)

#### Defined in

[socket-v2-sdk/src/client/models/NextTxResponse.ts:22](https://github.com/rugamoto/socket-v2-sdk/blob/b3c3e8d/src/client/models/NextTxResponse.ts#L22)

---

### done

• **done**: `boolean` = `false`

If the transaction is done

#### Defined in

[socket-v2-sdk/src/socketTx.ts:26](https://github.com/rugamoto/socket-v2-sdk/blob/b3c3e8d/src/socketTx.ts#L26)

---

### hash

• **hash**: `undefined` \| `string`

Hash associated with this socket transaction step

#### Defined in

[socket-v2-sdk/src/socketTx.ts:30](https://github.com/rugamoto/socket-v2-sdk/blob/b3c3e8d/src/socketTx.ts#L30)

---

### totalUserTx

• **totalUserTx**: `number`

Total number of transactions in Active Route.

#### Inherited from

[NextTxResponse](../interfaces/NextTxResponse.md).[totalUserTx](../interfaces/NextTxResponse.md#totalusertx)

#### Defined in

[socket-v2-sdk/src/client/models/NextTxResponse.ts:43](https://github.com/rugamoto/socket-v2-sdk/blob/b3c3e8d/src/client/models/NextTxResponse.ts#L43)

---

### txData

• **txData**: `string`

Calldata for transaction.

#### Inherited from

[NextTxResponse](../interfaces/NextTxResponse.md).[txData](../interfaces/NextTxResponse.md#txdata)

#### Defined in

[socket-v2-sdk/src/client/models/NextTxResponse.ts:26](https://github.com/rugamoto/socket-v2-sdk/blob/b3c3e8d/src/client/models/NextTxResponse.ts#L26)

---

### txTarget

• **txTarget**: `string`

Address to which transaction has to be sent.

#### Inherited from

[NextTxResponse](../interfaces/NextTxResponse.md).[txTarget](../interfaces/NextTxResponse.md#txtarget)

#### Defined in

[socket-v2-sdk/src/client/models/NextTxResponse.ts:18](https://github.com/rugamoto/socket-v2-sdk/blob/b3c3e8d/src/client/models/NextTxResponse.ts#L18)

---

### txType

• **txType**: [`TxType`](../enums/TxType.md)

Type of transaction.

#### Inherited from

[NextTxResponse](../interfaces/NextTxResponse.md).[txType](../interfaces/NextTxResponse.md#txtype)

#### Defined in

[socket-v2-sdk/src/client/models/NextTxResponse.ts:30](https://github.com/rugamoto/socket-v2-sdk/blob/b3c3e8d/src/client/models/NextTxResponse.ts#L30)

---

### userTxIndex

• **userTxIndex**: `number`

Index of transaction in Active Route. Index of the object in the userTxs array.

#### Inherited from

[NextTxResponse](../interfaces/NextTxResponse.md).[userTxIndex](../interfaces/NextTxResponse.md#usertxindex)

#### Defined in

[socket-v2-sdk/src/client/models/NextTxResponse.ts:39](https://github.com/rugamoto/socket-v2-sdk/blob/b3c3e8d/src/client/models/NextTxResponse.ts#L39)

---

### userTxType

• **userTxType**: [`UserTxType`](../enums/UserTxType.md)

Type of user transaction.

#### Inherited from

[NextTxResponse](../interfaces/NextTxResponse.md).[userTxType](../interfaces/NextTxResponse.md#usertxtype)

#### Defined in

[socket-v2-sdk/src/client/models/NextTxResponse.ts:14](https://github.com/rugamoto/socket-v2-sdk/blob/b3c3e8d/src/client/models/NextTxResponse.ts#L14)

---

### value

• **value**: `string`

Native token amount to be sent with transaction.

#### Inherited from

[NextTxResponse](../interfaces/NextTxResponse.md).[value](../interfaces/NextTxResponse.md#value)

#### Defined in

[socket-v2-sdk/src/client/models/NextTxResponse.ts:35](https://github.com/rugamoto/socket-v2-sdk/blob/b3c3e8d/src/client/models/NextTxResponse.ts#L35)

## Methods

### approvalRequired

▸ **approvalRequired**(): `Promise`<`boolean`\>

Whether an approval transaction is required.

#### Returns

`Promise`<`boolean`\>

True if required, otherwise false.

#### Defined in

[socket-v2-sdk/src/socketTx.ts:45](https://github.com/rugamoto/socket-v2-sdk/blob/b3c3e8d/src/socketTx.ts#L45)

---

### getApproveTransaction

▸ **getApproveTransaction**(): `Promise`<`null` \| { `data?`: `string` ; `from?`: `string` ; `to?`: `string` }\>

Get the apporval transaction data if it is required

#### Returns

`Promise`<`null` \| { `data?`: `string` ; `from?`: `string` ; `to?`: `string` }\>

Apporval data to be sent if required, otherwise null

#### Defined in

[socket-v2-sdk/src/socketTx.ts:80](https://github.com/rugamoto/socket-v2-sdk/blob/b3c3e8d/src/socketTx.ts#L80)

---

### getSendTransaction

▸ **getSendTransaction**(): `Promise`<{ `data`: `string` ; `to`: `string` ; `value`: `string` }\>

Get the transaction data

#### Returns

`Promise`<{ `data`: `string` ; `to`: `string` ; `value`: `string` }\>

Send transaction data

#### Defined in

[socket-v2-sdk/src/socketTx.ts:107](https://github.com/rugamoto/socket-v2-sdk/blob/b3c3e8d/src/socketTx.ts#L107)

---

### submit

▸ **submit**(`hash`): `Promise`<[`COMPLETED`](../enums/PrepareActiveRouteStatus.md#completed)\>

Submit the hash for this transaction and wait until it is marked as complete

#### Parameters

| Name   | Type     | Description                                  |
| :----- | :------- | :------------------------------------------- |
| `hash` | `string` | The hash for this transaction on the network |

#### Returns

`Promise`<[`COMPLETED`](../enums/PrepareActiveRouteStatus.md#completed)\>

Returns the final status "COMPLETED" once the transaction is complete

#### Defined in

[socket-v2-sdk/src/socketTx.ts:145](https://github.com/rugamoto/socket-v2-sdk/blob/b3c3e8d/src/socketTx.ts#L145)

# NextTxResponse

## Hierarchy

- **`NextTxResponse`**

  ↳ [`SocketTx`](../sdk/SocketTx.md)

## Table of contents

### Properties

- [activeRouteId](NextTxResponse.md#activerouteid)
- [approvalData](NextTxResponse.md#approvaldata)
- [chainId](NextTxResponse.md#chainid)
- [totalUserTx](NextTxResponse.md#totalusertx)
- [txData](NextTxResponse.md#txdata)
- [txTarget](NextTxResponse.md#txtarget)
- [txType](NextTxResponse.md#txtype)
- [userTxIndex](NextTxResponse.md#usertxindex)
- [userTxType](NextTxResponse.md#usertxtype)
- [value](NextTxResponse.md#value)

## Properties

### activeRouteId

• **activeRouteId**: `number`

Id of Active Route.

#### Defined in

[socket-v2-sdk/src/client/models/NextTxResponse.ts:10](https://github.com/SocketDotTech/socket-v2-sdk/blob/91d9fe3/src/client/models/NextTxResponse.ts#L10)

---

### approvalData

• **approvalData**: `null` \| [`ApprovalData`](../types.md#approvaldata)

#### Defined in

[socket-v2-sdk/src/client/models/NextTxResponse.ts:44](https://github.com/SocketDotTech/socket-v2-sdk/blob/91d9fe3/src/client/models/NextTxResponse.ts#L44)

---

### chainId

• **chainId**: [`ChainId`](../enums/ChainId.md)

Id of chain where transaction has to be sent.

#### Defined in

[socket-v2-sdk/src/client/models/NextTxResponse.ts:22](https://github.com/SocketDotTech/socket-v2-sdk/blob/91d9fe3/src/client/models/NextTxResponse.ts#L22)

---

### totalUserTx

• **totalUserTx**: `number`

Total number of transactions in Active Route.

#### Defined in

[socket-v2-sdk/src/client/models/NextTxResponse.ts:43](https://github.com/SocketDotTech/socket-v2-sdk/blob/91d9fe3/src/client/models/NextTxResponse.ts#L43)

---

### txData

• **txData**: `string`

Calldata for transaction.

#### Defined in

[socket-v2-sdk/src/client/models/NextTxResponse.ts:26](https://github.com/SocketDotTech/socket-v2-sdk/blob/91d9fe3/src/client/models/NextTxResponse.ts#L26)

---

### txTarget

• **txTarget**: `string`

Address to which transaction has to be sent.

#### Defined in

[socket-v2-sdk/src/client/models/NextTxResponse.ts:18](https://github.com/SocketDotTech/socket-v2-sdk/blob/91d9fe3/src/client/models/NextTxResponse.ts#L18)

---

### txType

• **txType**: [`TxType`](../enums/TxType.md)

Type of transaction.

#### Defined in

[socket-v2-sdk/src/client/models/NextTxResponse.ts:30](https://github.com/SocketDotTech/socket-v2-sdk/blob/91d9fe3/src/client/models/NextTxResponse.ts#L30)

---

### userTxIndex

• **userTxIndex**: `number`

Index of transaction in Active Route. Index of the object in the userTxs array.

#### Defined in

[socket-v2-sdk/src/client/models/NextTxResponse.ts:39](https://github.com/SocketDotTech/socket-v2-sdk/blob/91d9fe3/src/client/models/NextTxResponse.ts#L39)

---

### userTxType

• **userTxType**: [`UserTxType`](../enums/UserTxType.md)

Type of user transaction.

#### Defined in

[socket-v2-sdk/src/client/models/NextTxResponse.ts:14](https://github.com/SocketDotTech/socket-v2-sdk/blob/91d9fe3/src/client/models/NextTxResponse.ts#L14)

---

### value

• **value**: `string`

Native token amount to be sent with transaction.

#### Defined in

[socket-v2-sdk/src/client/models/NextTxResponse.ts:35](https://github.com/SocketDotTech/socket-v2-sdk/blob/91d9fe3/src/client/models/NextTxResponse.ts#L35)

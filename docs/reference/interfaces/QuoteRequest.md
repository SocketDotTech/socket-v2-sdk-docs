# QuoteRequest

## Hierarchy

- [`QuotePreferences`](QuotePreferences.md)

  ↳ **`QuoteRequest`**

## Table of contents

### Properties

- [bridgeWithGas](QuoteRequest.md#bridgewithgas)
- [disableSwapping](QuoteRequest.md#disableswapping)
- [excludeBridges](QuoteRequest.md#excludebridges)
- [excludeDexes](QuoteRequest.md#excludedexes)
- [fromAmount](QuoteRequest.md#fromamount)
- [fromChainId](QuoteRequest.md#fromchainid)
- [fromTokenAddress](QuoteRequest.md#fromtokenaddress)
- [includeBridges](QuoteRequest.md#includebridges)
- [includeDexes](QuoteRequest.md#includedexes)
- [isContractCall](QuoteRequest.md#iscontractcall)
- [maxUserTxs](QuoteRequest.md#maxusertxs)
- [recipient](QuoteRequest.md#recipient)
- [singleTxOnly](QuoteRequest.md#singletxonly)
- [sort](QuoteRequest.md#sort)
- [toChainId](QuoteRequest.md#tochainid)
- [toTokenAddress](QuoteRequest.md#totokenaddress)
- [uniqueRoutesPerBridge](QuoteRequest.md#uniqueroutesperbridge)
- [userAddress](QuoteRequest.md#useraddress)

## Properties

### bridgeWithGas

• `Optional` **bridgeWithGas**: `boolean`

include gas transfer with bridging tx

#### Inherited from

[QuotePreferences](QuotePreferences.md).[bridgeWithGas](QuotePreferences.md#bridgewithgas)

#### Defined in

[socket-v2-sdk/src/client/models/QuoteRequest.ts:20](https://github.com/rugamoto/socket-v2-sdk/blob/91d9fe3/src/client/models/QuoteRequest.ts#L20)

---

### disableSwapping

• `Optional` **disableSwapping**: `boolean`

Flag to specify if routes that have dex swap should be ignored.

#### Inherited from

[QuotePreferences](QuotePreferences.md).[disableSwapping](QuotePreferences.md#disableswapping)

#### Defined in

[socket-v2-sdk/src/client/models/SocketPreferences.ts:5](https://github.com/rugamoto/socket-v2-sdk/blob/91d9fe3/src/client/models/SocketPreferences.ts#L5)

---

### excludeBridges

• `Optional` **excludeBridges**: [`BridgeName`](../enums/BridgeName.md)[]

Specify Bridges that should be excluded in routes.
This option will be ignored if includeBridges is specified.

#### Inherited from

[QuotePreferences](QuotePreferences.md).[excludeBridges](QuotePreferences.md#excludebridges)

#### Defined in

[socket-v2-sdk/src/client/models/SocketPreferences.ts:15](https://github.com/rugamoto/socket-v2-sdk/blob/91d9fe3/src/client/models/SocketPreferences.ts#L15)

---

### excludeDexes

• `Optional` **excludeDexes**: [`Dexes`](../types.md#dexes)[]

Specify Dexes that should be excluded in routes.
This option will be ignored if includeDexes is specified.

#### Inherited from

[QuotePreferences](QuotePreferences.md).[excludeDexes](QuotePreferences.md#excludedexes)

#### Defined in

[socket-v2-sdk/src/client/models/SocketPreferences.ts:10](https://github.com/rugamoto/socket-v2-sdk/blob/91d9fe3/src/client/models/SocketPreferences.ts#L10)

---

### fromAmount

• **fromAmount**: `string`

Amount of sending tokens.

#### Defined in

[socket-v2-sdk/src/client/models/QuoteRequest.ts:33](https://github.com/rugamoto/socket-v2-sdk/blob/91d9fe3/src/client/models/QuoteRequest.ts#L33)

---

### fromChainId

• **fromChainId**: `number`

Chain id of source chain.

#### Defined in

[socket-v2-sdk/src/client/models/QuoteRequest.ts:25](https://github.com/rugamoto/socket-v2-sdk/blob/91d9fe3/src/client/models/QuoteRequest.ts#L25)

---

### fromTokenAddress

• **fromTokenAddress**: `string`

Token address on source chain.

#### Defined in

[socket-v2-sdk/src/client/models/QuoteRequest.ts:27](https://github.com/rugamoto/socket-v2-sdk/blob/91d9fe3/src/client/models/QuoteRequest.ts#L27)

---

### includeBridges

• `Optional` **includeBridges**: [`BridgeName`](../enums/BridgeName.md)[]

Specify Bridges that should be included in routes.

#### Inherited from

[QuotePreferences](QuotePreferences.md).[includeBridges](QuotePreferences.md#includebridges)

#### Defined in

[socket-v2-sdk/src/client/models/SocketPreferences.ts:12](https://github.com/rugamoto/socket-v2-sdk/blob/91d9fe3/src/client/models/SocketPreferences.ts#L12)

---

### includeDexes

• `Optional` **includeDexes**: [`Dexes`](../types.md#dexes)[]

Specify Dexes that should be included in routes.

#### Inherited from

[QuotePreferences](QuotePreferences.md).[includeDexes](QuotePreferences.md#includedexes)

#### Defined in

[socket-v2-sdk/src/client/models/SocketPreferences.ts:7](https://github.com/rugamoto/socket-v2-sdk/blob/91d9fe3/src/client/models/SocketPreferences.ts#L7)

---

### isContractCall

• `Optional` **isContractCall**: `boolean`

Only get quotes with that are compatible with contracts

#### Inherited from

[QuotePreferences](QuotePreferences.md).[isContractCall](QuotePreferences.md#iscontractcall)

#### Defined in

[socket-v2-sdk/src/client/models/QuoteRequest.ts:18](https://github.com/rugamoto/socket-v2-sdk/blob/91d9fe3/src/client/models/QuoteRequest.ts#L18)

---

### maxUserTxs

• `Optional` **maxUserTxs**: `string`

Maximum number of transactions.
This option will be ignored if singleTxOnly is marked as true.

#### Inherited from

[QuotePreferences](QuotePreferences.md).[maxUserTxs](QuotePreferences.md#maxusertxs)

#### Defined in

[socket-v2-sdk/src/client/models/QuoteRequest.ts:16](https://github.com/rugamoto/socket-v2-sdk/blob/91d9fe3/src/client/models/QuoteRequest.ts#L16)

---

### recipient

• `Optional` **recipient**: `string`

Address of recipient. This will be used to check approvals.

#### Defined in

[socket-v2-sdk/src/client/models/QuoteRequest.ts:37](https://github.com/rugamoto/socket-v2-sdk/blob/91d9fe3/src/client/models/QuoteRequest.ts#L37)

---

### singleTxOnly

• `Optional` **singleTxOnly**: `boolean`

Only get quotes with one user transaction to bridge.

#### Inherited from

[QuotePreferences](QuotePreferences.md).[singleTxOnly](QuotePreferences.md#singletxonly)

#### Defined in

[socket-v2-sdk/src/client/models/SocketPreferences.ts:17](https://github.com/rugamoto/socket-v2-sdk/blob/91d9fe3/src/client/models/SocketPreferences.ts#L17)

---

### sort

• `Optional` **sort**: [`SortOptions`](../enums/SortOptions.md)

Param to sort routes based on.

#### Inherited from

[QuotePreferences](QuotePreferences.md).[sort](QuotePreferences.md#sort)

#### Defined in

[socket-v2-sdk/src/client/models/QuoteRequest.ts:13](https://github.com/rugamoto/socket-v2-sdk/blob/91d9fe3/src/client/models/QuoteRequest.ts#L13)

---

### toChainId

• **toChainId**: `number`

Chain id of destination chain.

#### Defined in

[socket-v2-sdk/src/client/models/QuoteRequest.ts:29](https://github.com/rugamoto/socket-v2-sdk/blob/91d9fe3/src/client/models/QuoteRequest.ts#L29)

---

### toTokenAddress

• **toTokenAddress**: `string`

Token address on destination chain.

#### Defined in

[socket-v2-sdk/src/client/models/QuoteRequest.ts:31](https://github.com/rugamoto/socket-v2-sdk/blob/91d9fe3/src/client/models/QuoteRequest.ts#L31)

---

### uniqueRoutesPerBridge

• `Optional` **uniqueRoutesPerBridge**: `boolean`

Flag to return only best route per bridge using the sort criteria

#### Inherited from

[QuotePreferences](QuotePreferences.md).[uniqueRoutesPerBridge](QuotePreferences.md#uniqueroutesperbridge)

#### Defined in

[socket-v2-sdk/src/client/models/QuoteRequest.ts:11](https://github.com/rugamoto/socket-v2-sdk/blob/91d9fe3/src/client/models/QuoteRequest.ts#L11)

---

### userAddress

• **userAddress**: `string`

Address of user. This will be used to check approvals.

#### Defined in

[socket-v2-sdk/src/client/models/QuoteRequest.ts:35](https://github.com/rugamoto/socket-v2-sdk/blob/91d9fe3/src/client/models/QuoteRequest.ts#L35)

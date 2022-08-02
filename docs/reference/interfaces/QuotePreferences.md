# QuotePreferences

## Hierarchy

- [`SocketPreferences`](SocketPreferences.md)

  ↳ **`QuotePreferences`**

  ↳↳ [`QuoteRequest`](QuoteRequest.md)

## Table of contents

### Properties

- [bridgeWithGas](QuotePreferences.md#bridgewithgas)
- [disableSwapping](QuotePreferences.md#disableswapping)
- [excludeBridges](QuotePreferences.md#excludebridges)
- [excludeDexes](QuotePreferences.md#excludedexes)
- [includeBridges](QuotePreferences.md#includebridges)
- [includeDexes](QuotePreferences.md#includedexes)
- [isContractCall](QuotePreferences.md#iscontractcall)
- [maxUserTxs](QuotePreferences.md#maxusertxs)
- [singleTxOnly](QuotePreferences.md#singletxonly)
- [sort](QuotePreferences.md#sort)
- [uniqueRoutesPerBridge](QuotePreferences.md#uniqueroutesperbridge)

## Properties

### bridgeWithGas

• `Optional` **bridgeWithGas**: `boolean`

include gas transfer with bridging tx

#### Defined in

[socket-v2-sdk/src/client/models/QuoteRequest.ts:20](https://github.com/rugamoto/socket-v2-sdk/blob/91d9fe3/src/client/models/QuoteRequest.ts#L20)

---

### disableSwapping

• `Optional` **disableSwapping**: `boolean`

Flag to specify if routes that have dex swap should be ignored.

#### Inherited from

[SocketPreferences](SocketPreferences.md).[disableSwapping](SocketPreferences.md#disableswapping)

#### Defined in

[socket-v2-sdk/src/client/models/SocketPreferences.ts:5](https://github.com/rugamoto/socket-v2-sdk/blob/91d9fe3/src/client/models/SocketPreferences.ts#L5)

---

### excludeBridges

• `Optional` **excludeBridges**: [`BridgeName`](../enums/BridgeName.md)[]

Specify Bridges that should be excluded in routes.
This option will be ignored if includeBridges is specified.

#### Inherited from

[SocketPreferences](SocketPreferences.md).[excludeBridges](SocketPreferences.md#excludebridges)

#### Defined in

[socket-v2-sdk/src/client/models/SocketPreferences.ts:15](https://github.com/rugamoto/socket-v2-sdk/blob/91d9fe3/src/client/models/SocketPreferences.ts#L15)

---

### excludeDexes

• `Optional` **excludeDexes**: [`Dexes`](../types.md#dexes)[]

Specify Dexes that should be excluded in routes.
This option will be ignored if includeDexes is specified.

#### Inherited from

[SocketPreferences](SocketPreferences.md).[excludeDexes](SocketPreferences.md#excludedexes)

#### Defined in

[socket-v2-sdk/src/client/models/SocketPreferences.ts:10](https://github.com/rugamoto/socket-v2-sdk/blob/91d9fe3/src/client/models/SocketPreferences.ts#L10)

---

### includeBridges

• `Optional` **includeBridges**: [`BridgeName`](../enums/BridgeName.md)[]

Specify Bridges that should be included in routes.

#### Inherited from

[SocketPreferences](SocketPreferences.md).[includeBridges](SocketPreferences.md#includebridges)

#### Defined in

[socket-v2-sdk/src/client/models/SocketPreferences.ts:12](https://github.com/rugamoto/socket-v2-sdk/blob/91d9fe3/src/client/models/SocketPreferences.ts#L12)

---

### includeDexes

• `Optional` **includeDexes**: [`Dexes`](../types.md#dexes)[]

Specify Dexes that should be included in routes.

#### Inherited from

[SocketPreferences](SocketPreferences.md).[includeDexes](SocketPreferences.md#includedexes)

#### Defined in

[socket-v2-sdk/src/client/models/SocketPreferences.ts:7](https://github.com/rugamoto/socket-v2-sdk/blob/91d9fe3/src/client/models/SocketPreferences.ts#L7)

---

### isContractCall

• `Optional` **isContractCall**: `boolean`

Only get quotes with that are compatible with contracts

#### Defined in

[socket-v2-sdk/src/client/models/QuoteRequest.ts:18](https://github.com/rugamoto/socket-v2-sdk/blob/91d9fe3/src/client/models/QuoteRequest.ts#L18)

---

### maxUserTxs

• `Optional` **maxUserTxs**: `string`

Maximum number of transactions.
This option will be ignored if singleTxOnly is marked as true.

#### Defined in

[socket-v2-sdk/src/client/models/QuoteRequest.ts:16](https://github.com/rugamoto/socket-v2-sdk/blob/91d9fe3/src/client/models/QuoteRequest.ts#L16)

---

### singleTxOnly

• `Optional` **singleTxOnly**: `boolean`

Only get quotes with one user transaction to bridge.

#### Inherited from

[SocketPreferences](SocketPreferences.md).[singleTxOnly](SocketPreferences.md#singletxonly)

#### Defined in

[socket-v2-sdk/src/client/models/SocketPreferences.ts:17](https://github.com/rugamoto/socket-v2-sdk/blob/91d9fe3/src/client/models/SocketPreferences.ts#L17)

---

### sort

• `Optional` **sort**: [`SortOptions`](../enums/SortOptions.md)

Param to sort routes based on.

#### Defined in

[socket-v2-sdk/src/client/models/QuoteRequest.ts:13](https://github.com/rugamoto/socket-v2-sdk/blob/91d9fe3/src/client/models/QuoteRequest.ts#L13)

---

### uniqueRoutesPerBridge

• `Optional` **uniqueRoutesPerBridge**: `boolean`

Flag to return only best route per bridge using the sort criteria

#### Defined in

[socket-v2-sdk/src/client/models/QuoteRequest.ts:11](https://github.com/rugamoto/socket-v2-sdk/blob/91d9fe3/src/client/models/QuoteRequest.ts#L11)

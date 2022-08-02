# TokenListRequest

## Hierarchy

- [`SocketPreferences`](SocketPreferences.md)

  ↳ **`TokenListRequest`**

## Table of contents

### Properties

- [disableSwapping](TokenListRequest.md#disableswapping)
- [excludeBridges](TokenListRequest.md#excludebridges)
- [excludeDexes](TokenListRequest.md#excludedexes)
- [fromChainId](TokenListRequest.md#fromchainid)
- [includeBridges](TokenListRequest.md#includebridges)
- [includeDexes](TokenListRequest.md#includedexes)
- [isShortList](TokenListRequest.md#isshortlist)
- [singleTxOnly](TokenListRequest.md#singletxonly)
- [toChainId](TokenListRequest.md#tochainid)

## Properties

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

### fromChainId

• **fromChainId**: `number`

Id of source chain, e.g Optimism = 10

#### Defined in

[socket-v2-sdk/src/client/models/TokenListRequest.ts:5](https://github.com/rugamoto/socket-v2-sdk/blob/91d9fe3/src/client/models/TokenListRequest.ts#L5)

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

### isShortList

• `Optional` **isShortList**: `boolean`

To be Marked true if you want the shorter and more efficient token list.

#### Defined in

[socket-v2-sdk/src/client/models/TokenListRequest.ts:9](https://github.com/rugamoto/socket-v2-sdk/blob/91d9fe3/src/client/models/TokenListRequest.ts#L9)

---

### singleTxOnly

• `Optional` **singleTxOnly**: `boolean`

Only get quotes with one user transaction to bridge.

#### Inherited from

[SocketPreferences](SocketPreferences.md).[singleTxOnly](SocketPreferences.md#singletxonly)

#### Defined in

[socket-v2-sdk/src/client/models/SocketPreferences.ts:17](https://github.com/rugamoto/socket-v2-sdk/blob/91d9fe3/src/client/models/SocketPreferences.ts#L17)

---

### toChainId

• **toChainId**: `number`

Id of destination chain, e.g xDAI = 100

#### Defined in

[socket-v2-sdk/src/client/models/TokenListRequest.ts:7](https://github.com/rugamoto/socket-v2-sdk/blob/91d9fe3/src/client/models/TokenListRequest.ts#L7)

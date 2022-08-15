# SocketPreferences

## Hierarchy

- **`SocketPreferences`**

  ↳ [`QuotePreferences`](QuotePreferences.md)

  ↳ [`TokenListRequest`](TokenListRequest.md)

## Table of contents

### Properties

- [disableSwapping](SocketPreferences.md#disableswapping)
- [excludeBridges](SocketPreferences.md#excludebridges)
- [excludeDexes](SocketPreferences.md#excludedexes)
- [includeBridges](SocketPreferences.md#includebridges)
- [includeDexes](SocketPreferences.md#includedexes)
- [singleTxOnly](SocketPreferences.md#singletxonly)

## Properties

### disableSwapping

• `Optional` **disableSwapping**: `boolean`

Flag to specify if routes that have dex swap should be ignored.

#### Defined in

[socket-v2-sdk/src/client/models/SocketPreferences.ts:5](https://github.com/SocketDotTech/socket-v2-sdk/blob/91d9fe3/src/client/models/SocketPreferences.ts#L5)

---

### excludeBridges

• `Optional` **excludeBridges**: [`BridgeName`](../enums/BridgeName.md)[]

Specify Bridges that should be excluded in routes.
This option will be ignored if includeBridges is specified.

#### Defined in

[socket-v2-sdk/src/client/models/SocketPreferences.ts:15](https://github.com/SocketDotTech/socket-v2-sdk/blob/91d9fe3/src/client/models/SocketPreferences.ts#L15)

---

### excludeDexes

• `Optional` **excludeDexes**: [`Dexes`](../types.md#dexes)[]

Specify Dexes that should be excluded in routes.
This option will be ignored if includeDexes is specified.

#### Defined in

[socket-v2-sdk/src/client/models/SocketPreferences.ts:10](https://github.com/SocketDotTech/socket-v2-sdk/blob/91d9fe3/src/client/models/SocketPreferences.ts#L10)

---

### includeBridges

• `Optional` **includeBridges**: [`BridgeName`](../enums/BridgeName.md)[]

Specify Bridges that should be included in routes.

#### Defined in

[socket-v2-sdk/src/client/models/SocketPreferences.ts:12](https://github.com/SocketDotTech/socket-v2-sdk/blob/91d9fe3/src/client/models/SocketPreferences.ts#L12)

---

### includeDexes

• `Optional` **includeDexes**: [`Dexes`](../types.md#dexes)[]

Specify Dexes that should be included in routes.

#### Defined in

[socket-v2-sdk/src/client/models/SocketPreferences.ts:7](https://github.com/SocketDotTech/socket-v2-sdk/blob/91d9fe3/src/client/models/SocketPreferences.ts#L7)

---

### singleTxOnly

• `Optional` **singleTxOnly**: `boolean`

Only get quotes with one user transaction to bridge.

#### Defined in

[socket-v2-sdk/src/client/models/SocketPreferences.ts:17](https://github.com/SocketDotTech/socket-v2-sdk/blob/91d9fe3/src/client/models/SocketPreferences.ts#L17)

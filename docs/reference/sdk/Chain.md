# Chain

The chain object represents a supported chain

## Hierarchy

- [`ChainDetails`](../types.md#chaindetails)

  ↳ **`Chain`**

## Table of contents

### Constructors

- [constructor](Chain.md#constructor)

### Properties

- [chainId](Chain.md#chainid)
- [currency](Chain.md#currency)
- [explorers](Chain.md#explorers)
- [icon](Chain.md#icon)
- [isL1](Chain.md#isl1)
- [name](Chain.md#name)
- [receivingEnabled](Chain.md#receivingenabled)
- [rpcs](Chain.md#rpcs)
- [sendingEnabled](Chain.md#sendingenabled)

### Accessors

- [nativeToken](Chain.md#nativetoken)

## Constructors

### constructor

• **new Chain**(`chainDetails`)

#### Parameters

| Name           | Type                                       |
| :------------- | :----------------------------------------- |
| `chainDetails` | [`ChainDetails`](../types.md#chaindetails) |

#### Inherited from

ChainDetails.constructor

#### Defined in

[socket-v2-sdk/src/chain.ts:10](https://github.com/rugamoto/socket-v2-sdk/blob/b3c3e8d/src/chain.ts#L10)

## Properties

### chainId

• **chainId**: [`ChainId`](../enums/ChainId.md)

Id of chain.

#### Inherited from

ChainDetails.chainId

#### Defined in

[socket-v2-sdk/src/client/models/ChainDetails.ts:8](https://github.com/rugamoto/socket-v2-sdk/blob/b3c3e8d/src/client/models/ChainDetails.ts#L8)

---

### currency

• **currency**: [`GasTokenDetails`](../types.md#gastokendetails)

#### Inherited from

ChainDetails.currency

#### Defined in

[socket-v2-sdk/src/client/models/ChainDetails.ts:29](https://github.com/rugamoto/socket-v2-sdk/blob/b3c3e8d/src/client/models/ChainDetails.ts#L29)

---

### explorers

• **explorers**: `string`[]

#### Inherited from

ChainDetails.explorers

#### Defined in

[socket-v2-sdk/src/client/models/ChainDetails.ts:31](https://github.com/rugamoto/socket-v2-sdk/blob/b3c3e8d/src/client/models/ChainDetails.ts#L31)

---

### icon

• **icon**: `string`

URL for icon of chain.

#### Inherited from

ChainDetails.icon

#### Defined in

[socket-v2-sdk/src/client/models/ChainDetails.ts:16](https://github.com/rugamoto/socket-v2-sdk/blob/b3c3e8d/src/client/models/ChainDetails.ts#L16)

---

### isL1

• **isL1**: `boolean`

Flag indicating whether the chain is L1.

#### Inherited from

ChainDetails.isL1

#### Defined in

[socket-v2-sdk/src/client/models/ChainDetails.ts:20](https://github.com/rugamoto/socket-v2-sdk/blob/b3c3e8d/src/client/models/ChainDetails.ts#L20)

---

### name

• **name**: `string`

Name of chain.

#### Inherited from

ChainDetails.name

#### Defined in

[socket-v2-sdk/src/client/models/ChainDetails.ts:12](https://github.com/rugamoto/socket-v2-sdk/blob/b3c3e8d/src/client/models/ChainDetails.ts#L12)

---

### receivingEnabled

• **receivingEnabled**: `boolean`

Flag indicating whether receiving of tokens is supported to chain.

#### Inherited from

ChainDetails.receivingEnabled

#### Defined in

[socket-v2-sdk/src/client/models/ChainDetails.ts:28](https://github.com/rugamoto/socket-v2-sdk/blob/b3c3e8d/src/client/models/ChainDetails.ts#L28)

---

### rpcs

• **rpcs**: `string`[]

#### Inherited from

ChainDetails.rpcs

#### Defined in

[socket-v2-sdk/src/client/models/ChainDetails.ts:30](https://github.com/rugamoto/socket-v2-sdk/blob/b3c3e8d/src/client/models/ChainDetails.ts#L30)

---

### sendingEnabled

• **sendingEnabled**: `boolean`

Flag indicating whether sending of tokens is supported from chain.

#### Inherited from

ChainDetails.sendingEnabled

#### Defined in

[socket-v2-sdk/src/client/models/ChainDetails.ts:24](https://github.com/rugamoto/socket-v2-sdk/blob/b3c3e8d/src/client/models/ChainDetails.ts#L24)

## Accessors

### nativeToken

• `get` **nativeToken**(): [`Token`](../types.md#token)

The native token of the chain

#### Returns

[`Token`](../types.md#token)

#### Defined in

[socket-v2-sdk/src/chain.ts:17](https://github.com/rugamoto/socket-v2-sdk/blob/b3c3e8d/src/chain.ts#L17)

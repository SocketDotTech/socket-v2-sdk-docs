# TokenList

The TokenList represents a list of tokens for a given chain

## Table of contents

### Constructors

- [constructor](TokenList.md#constructor)

### Properties

- [chainId](TokenList.md#chainid)
- [tokens](TokenList.md#tokens)

### Accessors

- [nativeToken](TokenList.md#nativetoken)

### Methods

- [tokenByAddress](TokenList.md#tokenbyaddress)
- [tokenBySymbol](TokenList.md#tokenbysymbol)

## Constructors

### constructor

• **new TokenList**(`chainId`, `tokens`)

#### Parameters

| Name      | Type                             |
| :-------- | :------------------------------- |
| `chainId` | [`ChainId`](../enums/ChainId.md) |
| `tokens`  | [`Token`](../types.md#token)[]   |

#### Defined in

[socket-v2-sdk/src/tokenList.ts:12](https://github.com/SocketDotTech/socket-v2-sdk/blob/b3c3e8d/src/tokenList.ts#L12)

## Properties

### chainId

• **chainId**: [`ChainId`](../enums/ChainId.md)

#### Defined in

[socket-v2-sdk/src/tokenList.ts:10](https://github.com/SocketDotTech/socket-v2-sdk/blob/b3c3e8d/src/tokenList.ts#L10)

---

### tokens

• **tokens**: [`Token`](../types.md#token)[]

#### Defined in

[socket-v2-sdk/src/tokenList.ts:9](https://github.com/SocketDotTech/socket-v2-sdk/blob/b3c3e8d/src/tokenList.ts#L9)

## Accessors

### nativeToken

• `get` **nativeToken**(): [`Token`](../types.md#token)

The native token of the chain

#### Returns

[`Token`](../types.md#token)

#### Defined in

[socket-v2-sdk/src/tokenList.ts:20](https://github.com/SocketDotTech/socket-v2-sdk/blob/b3c3e8d/src/tokenList.ts#L20)

## Methods

### tokenByAddress

▸ **tokenByAddress**(`address`): `undefined` \| [`Token`](../types.md#token)

Retrieve token by its address

#### Parameters

| Name      | Type     | Description   |
| :-------- | :------- | :------------ |
| `address` | `string` | token address |

#### Returns

`undefined` \| [`Token`](../types.md#token)

token object

#### Defined in

[socket-v2-sdk/src/tokenList.ts:31](https://github.com/SocketDotTech/socket-v2-sdk/blob/b3c3e8d/src/tokenList.ts#L31)

---

### tokenBySymbol

▸ **tokenBySymbol**(`symbol`): `undefined` \| [`Token`](../types.md#token)

Retrieve token by its symbol

#### Parameters

| Name     | Type     | Description           |
| :------- | :------- | :-------------------- |
| `symbol` | `string` | symbol. Example: USDC |

#### Returns

`undefined` \| [`Token`](../types.md#token)

token object

#### Defined in

[socket-v2-sdk/src/tokenList.ts:40](https://github.com/SocketDotTech/socket-v2-sdk/blob/b3c3e8d/src/tokenList.ts#L40)

# TokenLists

## Table of contents

### Constructors

- [constructor](TokenLists.md#constructor)

### Methods

- [getFromTokenList](TokenLists.md#getfromtokenlist)
- [getToTokenList](TokenLists.md#gettotokenlist)

## Constructors

### constructor

• **new TokenLists**()

## Methods

### getFromTokenList

▸ `Static` **getFromTokenList**(`__namedParameters`): [`CancelablePromise`](../client/CancelablePromise.md)<[`TokenListOutputDTO`](../types.md#tokenlistoutputdto)\>

**`throws`** ApiError

#### Parameters

| Name                | Type                                                    |
| :------------------ | :------------------------------------------------------ |
| `__namedParameters` | [`TokenListRequest`](../interfaces/TokenListRequest.md) |

#### Returns

[`CancelablePromise`](../client/CancelablePromise.md)<[`TokenListOutputDTO`](../types.md#tokenlistoutputdto)\>

TokenListOutputDTO All Supported token by a given chainId

#### Defined in

[socket-v2-sdk/src/client/services/TokenLists.ts:13](https://github.com/rugamoto/socket-v2-sdk/blob/91d9fe3/src/client/services/TokenLists.ts#L13)

---

### getToTokenList

▸ `Static` **getToTokenList**(`__namedParameters`): [`CancelablePromise`](../client/CancelablePromise.md)<[`TokenListOutputDTO`](../types.md#tokenlistoutputdto)\>

**`throws`** ApiError

#### Parameters

| Name                | Type                                                    |
| :------------------ | :------------------------------------------------------ |
| `__namedParameters` | [`TokenListRequest`](../interfaces/TokenListRequest.md) |

#### Returns

[`CancelablePromise`](../client/CancelablePromise.md)<[`TokenListOutputDTO`](../types.md#tokenlistoutputdto)\>

TokenListOutputDTO All Supported token by a given route

#### Defined in

[socket-v2-sdk/src/client/services/TokenLists.ts:48](https://github.com/rugamoto/socket-v2-sdk/blob/91d9fe3/src/client/services/TokenLists.ts#L48)

# Supported

## Table of contents

### Constructors

- [constructor](Supported.md#constructor)

### Methods

- [getAllBridges](Supported.md#getallbridges)
- [getAllSupportedChains](Supported.md#getallsupportedchains)
- [getIfTokenIsSupported](Supported.md#getiftokenissupported)

## Constructors

### constructor

• **new Supported**()

## Methods

### getAllBridges

▸ `Static` **getAllBridges**(): [`CancelablePromise`](../client/CancelablePromise.md)<[`SupportedBridgesOutputDTO`](../types.md#supportedbridgesoutputdto)\>

**`throws`** ApiError

#### Returns

[`CancelablePromise`](../client/CancelablePromise.md)<[`SupportedBridgesOutputDTO`](../types.md#supportedbridgesoutputdto)\>

SupportedBridgesOutputDTO All Supported Bridges

#### Defined in

[socket-v2-sdk/src/client/services/Supported.ts:14](https://github.com/rugamoto/socket-v2-sdk/blob/91d9fe3/src/client/services/Supported.ts#L14)

---

### getAllSupportedChains

▸ `Static` **getAllSupportedChains**(): [`CancelablePromise`](../client/CancelablePromise.md)<[`SupportedChainsOutputDTO`](../types.md#supportedchainsoutputdto)\>

**`throws`** ApiError

#### Returns

[`CancelablePromise`](../client/CancelablePromise.md)<[`SupportedChainsOutputDTO`](../types.md#supportedchainsoutputdto)\>

SupportedChainsOutputDTO All Supported Chains by Movr

#### Defined in

[socket-v2-sdk/src/client/services/Supported.ts:25](https://github.com/rugamoto/socket-v2-sdk/blob/91d9fe3/src/client/services/Supported.ts#L25)

---

### getIfTokenIsSupported

▸ `Static` **getIfTokenIsSupported**(`__namedParameters`): [`CancelablePromise`](../client/CancelablePromise.md)<[`SupportedChainsOutputDTO`](../types.md#supportedchainsoutputdto)\>

**`throws`** ApiError

#### Parameters

| Name                        | Type                             | Description                    |
| :-------------------------- | :------------------------------- | :----------------------------- |
| `__namedParameters`         | `Object`                         | -                              |
| `__namedParameters.address` | `string`                         | Contract address of the token  |
| `__namedParameters.chainId` | [`ChainId`](../enums/ChainId.md) | Id of chain, e.g Optimism = 10 |

#### Returns

[`CancelablePromise`](../client/CancelablePromise.md)<[`SupportedChainsOutputDTO`](../types.md#supportedchainsoutputdto)\>

SupportedChainsOutputDTO Get if token is supported

#### Defined in

[socket-v2-sdk/src/client/services/Supported.ts:39](https://github.com/rugamoto/socket-v2-sdk/blob/91d9fe3/src/client/services/Supported.ts#L39)

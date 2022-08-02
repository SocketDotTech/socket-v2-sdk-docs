# Balances

## Table of contents

### Constructors

- [constructor](Balances.md#constructor)

### Methods

- [getBalance](Balances.md#getbalance)
- [getBalances](Balances.md#getbalances)

## Constructors

### constructor

• **new Balances**()

## Methods

### getBalance

▸ `Static` **getBalance**(`__namedParameters`): [`CancelablePromise`](../client/CancelablePromise.md)<[`TokenBalanceReponseDTO`](../types.md#tokenbalancereponsedto)\>

**`throws`** ApiError

#### Parameters

| Name                             | Type                             | Description                                                     |
| :------------------------------- | :------------------------------- | :-------------------------------------------------------------- |
| `__namedParameters`              | `Object`                         | -                                                               |
| `__namedParameters.chainId`      | [`ChainId`](../enums/ChainId.md) | ID of chain, e.g Ethereum Mainnet = 1                           |
| `__namedParameters.tokenAddress` | `string`                         | Token contract address on network, e.g USDC on Ethereum Mainnet |
| `__namedParameters.userAddress`  | `string`                         | Address of the user                                             |

#### Returns

[`CancelablePromise`](../client/CancelablePromise.md)<[`TokenBalanceReponseDTO`](../types.md#tokenbalancereponsedto)\>

TokenBalanceReponseDTO Returns the balance of the token on any given chain

#### Defined in

[socket-v2-sdk/src/client/services/Balances.ts:31](https://github.com/rugamoto/socket-v2-sdk/blob/91d9fe3/src/client/services/Balances.ts#L31)

---

### getBalances

▸ `Static` **getBalances**(`__namedParameters`): [`CancelablePromise`](../client/CancelablePromise.md)<[`Balance`](../types.md#balance)\>

**`throws`** ApiError

#### Parameters

| Name                            | Type     |
| :------------------------------ | :------- |
| `__namedParameters`             | `Object` |
| `__namedParameters.userAddress` | `string` |

#### Returns

[`CancelablePromise`](../client/CancelablePromise.md)<[`Balance`](../types.md#balance)\>

Balance Returns the balance of all tokens for a user address on all supported chains

#### Defined in

[socket-v2-sdk/src/client/services/Balances.ts:14](https://github.com/rugamoto/socket-v2-sdk/blob/91d9fe3/src/client/services/Balances.ts#L14)

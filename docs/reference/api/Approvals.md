# Approvals

## Table of contents

### Constructors

- [constructor](Approvals.md#constructor)

### Methods

- [fetchApprovals](Approvals.md#fetchapprovals)
- [fetchApprovalsCalldata](Approvals.md#fetchapprovalscalldata)

## Constructors

### constructor

• **new Approvals**()

## Methods

### fetchApprovals

▸ `Static` **fetchApprovals**(`__namedParameters`): [`CancelablePromise`](../client/CancelablePromise.md)<[`ApprovalOutputDTO`](../types.md#approvaloutputdto)\>

**`throws`** ApiError

#### Parameters

| Name                                | Type                             | Description                                       |
| :---------------------------------- | :------------------------------- | :------------------------------------------------ |
| `__namedParameters`                 | `Object`                         | -                                                 |
| `__namedParameters.allowanceTarget` | `string`                         | Address whose spending allowance is to be checked |
| `__namedParameters.chainId`         | [`ChainId`](../enums/ChainId.md) | ID of chain, e.g Ethereum Mainnet = 1             |
| `__namedParameters.owner`           | `string`                         | Wallet address of token holder                    |
| `__namedParameters.tokenAddress`    | `string`                         | Contract address of token                         |

#### Returns

[`CancelablePromise`](../client/CancelablePromise.md)<[`ApprovalOutputDTO`](../types.md#approvaloutputdto)\>

ApprovalOutputDTO Gives approval values of given tokens for a given owner & chainId

#### Defined in

[socket-v2-sdk/src/client/services/Approvals.ts:14](https://github.com/SocketDotTech/socket-v2-sdk/blob/91d9fe3/src/client/services/Approvals.ts#L14)

---

### fetchApprovalsCalldata

▸ `Static` **fetchApprovalsCalldata**(`__namedParameters`): [`CancelablePromise`](../client/CancelablePromise.md)<[`ApprovalTxOutputDTO`](../types.md#approvaltxoutputdto)\>

**`throws`** ApiError

#### Parameters

| Name                                | Type                             | Description                                           |
| :---------------------------------- | :------------------------------- | :---------------------------------------------------- |
| `__namedParameters`                 | `Object`                         | -                                                     |
| `__namedParameters.allowanceTarget` | `string`                         | Address whose spending allowance is to be checked     |
| `__namedParameters.amount`          | `string`                         | Amount of tokens to approve, e.g 10 USDC (6 decimals) |
| `__namedParameters.chainId`         | [`ChainId`](../enums/ChainId.md) | ID of chain, e.g Ethereum Mainnet = 1                 |
| `__namedParameters.owner`           | `string`                         | Wallet address of token holder                        |
| `__namedParameters.tokenAddress`    | `string`                         | Contract address of token                             |

#### Returns

[`CancelablePromise`](../client/CancelablePromise.md)<[`ApprovalTxOutputDTO`](../types.md#approvaltxoutputdto)\>

ApprovalTxOutputDTO Return the Approval Tx Data for the given params.

#### Defined in

[socket-v2-sdk/src/client/services/Approvals.ts:48](https://github.com/SocketDotTech/socket-v2-sdk/blob/91d9fe3/src/client/services/Approvals.ts#L48)

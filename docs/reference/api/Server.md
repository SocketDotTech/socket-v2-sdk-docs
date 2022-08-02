# Server

## Table of contents

### Constructors

- [constructor](Server.md#constructor)

### Methods

- [getBridgingStatus](Server.md#getbridgingstatus)
- [getGasPrice](Server.md#getgasprice)
- [getHealth](Server.md#gethealth)
- [getHealthRpc](Server.md#gethealthrpc)
- [getSingleTx](Server.md#getsingletx)
- [getTokenPrice](Server.md#gettokenprice)
- [getTransactionReceipt](Server.md#gettransactionreceipt)

## Constructors

### constructor

• **new Server**()

## Methods

### getBridgingStatus

▸ `Static` **getBridgingStatus**(`__namedParameters`): [`CancelablePromise`](../client/CancelablePromise.md)<[`BridgeStatusResponseDTO`](../types.md#bridgestatusresponsedto)\>

**`throws`** ApiError

#### Parameters

| Name                                | Type                                   | Description                                                               |
| :---------------------------------- | :------------------------------------- | :------------------------------------------------------------------------ |
| `__namedParameters`                 | `Object`                               | -                                                                         |
| `__namedParameters.bridgeName?`     | [`BridgeName`](../enums/BridgeName.md) | Name of the bridge used while bridging.                                   |
| `__namedParameters.fromChainId`     | `number`                               | ID of source chain, e.g Ethereum Mainnet = 1                              |
| `__namedParameters.toChainId`       | `number`                               | ID of destination chain, e.g Ethereum Mainnet = 1                         |
| `__namedParameters.transactionHash` | `string`                               | Transaction hash originating from the source chain while bridging assets. |

#### Returns

[`CancelablePromise`](../client/CancelablePromise.md)<[`BridgeStatusResponseDTO`](../types.md#bridgestatusresponsedto)\>

BridgeStatusResponseDTO Returns the status of the bridging transaction if completed or pending.

#### Defined in

[socket-v2-sdk/src/client/services/Server.ts:105](https://github.com/rugamoto/socket-v2-sdk/blob/91d9fe3/src/client/services/Server.ts#L105)

---

### getGasPrice

▸ `Static` **getGasPrice**(`__namedParameters`): [`CancelablePromise`](../client/CancelablePromise.md)<[`GasPriceResponseDTO`](../types.md#gaspriceresponsedto)\>

**`throws`** ApiError

#### Parameters

| Name                        | Type                             | Description                           |
| :-------------------------- | :------------------------------- | :------------------------------------ |
| `__namedParameters`         | `Object`                         | -                                     |
| `__namedParameters.chainId` | [`ChainId`](../enums/ChainId.md) | ID of chain, e.g Ethereum Mainnet = 1 |

#### Returns

[`CancelablePromise`](../client/CancelablePromise.md)<[`GasPriceResponseDTO`](../types.md#gaspriceresponsedto)\>

GasPriceResponseDTO Current gas prices for a chain

#### Defined in

[socket-v2-sdk/src/client/services/Server.ts:42](https://github.com/rugamoto/socket-v2-sdk/blob/91d9fe3/src/client/services/Server.ts#L42)

---

### getHealth

▸ `Static` **getHealth**(): [`CancelablePromise`](../client/CancelablePromise.md)<[`HealthResponseDTO`](../types.md#healthresponsedto)\>

**`throws`** ApiError

#### Returns

[`CancelablePromise`](../client/CancelablePromise.md)<[`HealthResponseDTO`](../types.md#healthresponsedto)\>

HealthResponseDTO Health Check for Fund Movr API

#### Defined in

[socket-v2-sdk/src/client/services/Server.ts:20](https://github.com/rugamoto/socket-v2-sdk/blob/91d9fe3/src/client/services/Server.ts#L20)

---

### getHealthRpc

▸ `Static` **getHealthRpc**(): [`CancelablePromise`](../client/CancelablePromise.md)<`any`\>

**`throws`** ApiError

#### Returns

[`CancelablePromise`](../client/CancelablePromise.md)<`any`\>

any Health Check for Fund Movr API RPCS

#### Defined in

[socket-v2-sdk/src/client/services/Server.ts:31](https://github.com/rugamoto/socket-v2-sdk/blob/91d9fe3/src/client/services/Server.ts#L31)

---

### getSingleTx

▸ `Static` **getSingleTx**(`__namedParameters`): [`CancelablePromise`](../client/CancelablePromise.md)<[`SingleTxOutputDTO`](../types.md#singletxoutputdto)\>

**`throws`** ApiError

#### Parameters

| Name                            | Type                                     |
| :------------------------------ | :--------------------------------------- |
| `__namedParameters`             | `Object`                                 |
| `__namedParameters.requestBody` | [`SingleTxDTO`](../types.md#singletxdto) |

#### Returns

[`CancelablePromise`](../client/CancelablePromise.md)<[`SingleTxOutputDTO`](../types.md#singletxoutputdto)\>

SingleTxOutputDTO Get the tx details for the route.

#### Defined in

[socket-v2-sdk/src/client/services/Server.ts:85](https://github.com/rugamoto/socket-v2-sdk/blob/91d9fe3/src/client/services/Server.ts#L85)

---

### getTokenPrice

▸ `Static` **getTokenPrice**(`__namedParameters`): [`CancelablePromise`](../client/CancelablePromise.md)<[`TokenPriceResponseDTO`](../types.md#tokenpriceresponsedto)\>

**`throws`** ApiError

#### Parameters

| Name                             | Type                             | Description                                                     |
| :------------------------------- | :------------------------------- | :-------------------------------------------------------------- |
| `__namedParameters`              | `Object`                         | -                                                               |
| `__namedParameters.chainId`      | [`ChainId`](../enums/ChainId.md) | ID of chain, e.g Ethereum Mainnet = 1                           |
| `__namedParameters.tokenAddress` | `string`                         | Token contract address on network, e.g USDC on Ethereum Mainnet |

#### Returns

[`CancelablePromise`](../client/CancelablePromise.md)<[`TokenPriceResponseDTO`](../types.md#tokenpriceresponsedto)\>

TokenPriceResponseDTO Returns price of token for a given chain

#### Defined in

[socket-v2-sdk/src/client/services/Server.ts:61](https://github.com/rugamoto/socket-v2-sdk/blob/91d9fe3/src/client/services/Server.ts#L61)

---

### getTransactionReceipt

▸ `Static` **getTransactionReceipt**(`__namedParameters`): [`CancelablePromise`](../client/CancelablePromise.md)<[`TransactionReceiptResponseDTO`](../types.md#transactionreceiptresponsedto)\>

**`throws`** ApiError

#### Parameters

| Name                                | Type                             | Description                                                               |
| :---------------------------------- | :------------------------------- | :------------------------------------------------------------------------ |
| `__namedParameters`                 | `Object`                         | -                                                                         |
| `__namedParameters.chainId`         | [`ChainId`](../enums/ChainId.md) | ID of source chain, e.g Ethereum Mainnet = 1                              |
| `__namedParameters.transactionHash` | `string`                         | Transaction hash originating from the source chain while bridging assets. |

#### Returns

[`CancelablePromise`](../client/CancelablePromise.md)<[`TransactionReceiptResponseDTO`](../types.md#transactionreceiptresponsedto)\>

TransactionReceiptResponseDTO Returns the receipt of the transaction.

#### Defined in

[socket-v2-sdk/src/client/services/Server.ts:139](https://github.com/rugamoto/socket-v2-sdk/blob/91d9fe3/src/client/services/Server.ts#L139)

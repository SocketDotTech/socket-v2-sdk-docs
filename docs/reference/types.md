# Types

## Table of contents

### Enumerations

- [ActiveRouteStatus](enums/ActiveRouteStatus.md)
- [BridgeErrorStatus](enums/BridgeErrorStatus.md)
- [BridgeName](enums/BridgeName.md)
- [ChainId](enums/ChainId.md)
- [PrepareActiveRouteStatus](enums/PrepareActiveRouteStatus.md)
- [SortOptions](enums/SortOptions.md)
- [TxStatus](enums/TxStatus.md)
- [TxType](enums/TxType.md)
- [UserTxType](enums/UserTxType.md)

### Classes

- [ApiError](client/ApiError.md)
- [Approvals](api/Approvals.md)
- [Balances](api/Balances.md)
- [CancelError](client/CancelError.md)
- [CancelablePromise](client/../client/CancelablePromise.md)
- [Chain](sdk/Chain.md)
- [Path](sdk/Path.md)
- [Quotes](api/Quotes.md)
- [Routes](api/Routes.md)
- [Server](api/Server.md)
- [Socket](sdk/Socket.md)
- [SocketTx](sdk/SocketTx.md)
- [Supported](api/Supported.md)
- [TokenList](sdk/TokenList.md)
- [TokenLists](api/TokenLists.md)
- [Web3ConnectedSocket](sdk/Web3ConnectedSocket.md)

### Interfaces

- [ActiveRoutesRequest](interfaces/ActiveRoutesRequest.md)
- [AddEthereumChainParameters](interfaces/AddEthereumChainParameters.md)
- [EventCallbacks](interfaces/EventCallbacks.md)
- [NextTxResponse](interfaces/NextTxResponse.md)
- [QuoteParams](interfaces/QuoteParams.md)
- [QuotePreferences](interfaces/QuotePreferences.md)
- [QuoteRequest](interfaces/QuoteRequest.md)
- [RefuelData](interfaces/RefuelData.md)
- [SocketOptions](interfaces/SocketOptions.md)
- [SocketPreferences](interfaces/SocketPreferences.md)
- [SocketQuote](interfaces/SocketQuote.md)
- [TokenListRequest](interfaces/TokenListRequest.md)

### Type Aliases

- [ActiveRouteOutputDTO](types.md#activerouteoutputdto)
- [ActiveRouteResponse](types.md#activerouteresponse)
- [ActiveRoutesOutputDTO](types.md#activeroutesoutputdto)
- [ApprovalData](types.md#approvaldata)
- [ApprovalOutputDTO](types.md#approvaloutputdto)
- [ApprovalTxOutputDTO](types.md#approvaltxoutputdto)
- [Balance](types.md#balance)
- [BalanceResult](types.md#balanceresult)
- [BridgeDetails](types.md#bridgedetails)
- [BridgeRouteErrors](types.md#bridgerouteerrors)
- [BridgeStatusResponse](types.md#bridgestatusresponse)
- [BridgeStatusResponseDTO](types.md#bridgestatusresponsedto)
- [ChainDetails](types.md#chaindetails)
- [ChainGasBalances](types.md#chaingasbalances)
- [ChainSwitchDoneCallback](types.md#chainswitchdonecallback)
- [Dexes](types.md#dexes)
- [GasFee](types.md#gasfee)
- [GasPriceResponseDTO](types.md#gaspriceresponsedto)
- [GasTokenDetails](types.md#gastokendetails)
- [HealthResponseDTO](types.md#healthresponsedto)
- [MinGasBalances](types.md#mingasbalances)
- [NextTxOutputDTO](types.md#nexttxoutputdto)
- [OpenAPIConfig](types.md#openapiconfig)
- [Quote](types.md#quote)
- [QuoteOutputDTO](types.md#quoteoutputdto)
- [Route](types.md#route)
- [RouteStatusOutputDTO](types.md#routestatusoutputdto)
- [SingleTxDTO](types.md#singletxdto)
- [SingleTxOutputDTO](types.md#singletxoutputdto)
- [SingleTxResponse](types.md#singletxresponse)
- [SocketTxDoneCallback](types.md#sockettxdonecallback)
- [StartActiveRouteInputDTO](types.md#startactiverouteinputdto)
- [Step](types.md#step)
- [SupportedBridgesOutputDTO](types.md#supportedbridgesoutputdto)
- [SupportedChainsOutputDTO](types.md#supportedchainsoutputdto)
- [Token](types.md#token)
- [TokenBalanceReponseDTO](types.md#tokenbalancereponsedto)
- [TokenListOutputDTO](types.md#tokenlistoutputdto)
- [TokenPriceResponseDTO](types.md#tokenpriceresponsedto)
- [TransactionReceiptResponseDTO](types.md#transactionreceiptresponsedto)
- [TxDoneCallback](types.md#txdonecallback)
- [UserTx](types.md#usertx)

### Variables

- [OpenAPI](types.md#openapi)

## Type Aliases

### ActiveRouteOutputDTO

Ƭ **ActiveRouteOutputDTO**: `Object`

#### Type declaration

| Name      | Type                                                  | Description             |
| :-------- | :---------------------------------------------------- | :---------------------- |
| `result`  | [`ActiveRouteResponse`](types.md#activerouteresponse) | -                       |
| `success` | `boolean`                                             | Status of API response. |

#### Defined in

[socket-v2-sdk/src/client/models/ActiveRouteOutputDTO.ts:3](https://github.com/rugamoto/socket-v2-sdk/blob/91d9fe3/src/client/models/ActiveRouteOutputDTO.ts#L3)

---

### ActiveRouteResponse

Ƭ **ActiveRouteResponse**: `Object`

#### Type declaration

| Name                 | Type                                              | Description                                   |
| :------------------- | :------------------------------------------------ | :-------------------------------------------- |
| `activeRouteId`      | `number`                                          | Id of the Active Route.                       |
| `createdAt`          | `string`                                          | Timestamp of Route start.                     |
| `currentUserTxIndex` | `number`                                          | Index of current tx in userTxs array.         |
| `fromAmount`         | `string`                                          | Amount of sending tokens.                     |
| `fromAsset`          | [`Token`](types.md#token)                         | -                                             |
| `fromAssetAddress`   | `string`                                          | Address of token on source chain.             |
| `fromChainId`        | `number`                                          | Id of source chain.                           |
| `routeStatus`        | [`ActiveRouteStatus`](enums/ActiveRouteStatus.md) | Status of the Active Route.                   |
| `toAmount`           | `string`                                          | Approximate amount of receiving tokens.       |
| `toAsset`            | [`Token`](types.md#token)                         | -                                             |
| `toAssetAddress`     | `string`                                          | Address of token on destination chain.        |
| `toChainId`          | `number`                                          | Id of destination chain.                      |
| `totalUserTx`        | `number`                                          | Total number of txs required in Active Route. |
| `updatedAt`          | `string`                                          | Timestamp of last route update.               |
| `userAddress`        | `string`                                          | Address of user doing the Active Route.       |
| `userTxs`            | [`UserTx`](types.md#usertx)[]                     | Array of user txs.                            |

#### Defined in

[socket-v2-sdk/src/client/models/ActiveRouteResponse.ts:9](https://github.com/rugamoto/socket-v2-sdk/blob/91d9fe3/src/client/models/ActiveRouteResponse.ts#L9)

---

### ActiveRoutesOutputDTO

Ƭ **ActiveRoutesOutputDTO**: `Object`

#### Type declaration

| Name                             | Type                                                                                                                                                              | Description             |
| :------------------------------- | :---------------------------------------------------------------------------------------------------------------------------------------------------------------- | :---------------------- |
| `result`                         | { `activeRoutes`: [`ActiveRouteResponse`](types.md#activerouteresponse)[] ; `pagination`: { `limit`: `number` ; `offset`: `number` ; `totalRecords`: `number` } } | -                       |
| `result.activeRoutes`            | [`ActiveRouteResponse`](types.md#activerouteresponse)[]                                                                                                           | -                       |
| `result.pagination`              | { `limit`: `number` ; `offset`: `number` ; `totalRecords`: `number` }                                                                                             | -                       |
| `result.pagination.limit`        | `number`                                                                                                                                                          | -                       |
| `result.pagination.offset`       | `number`                                                                                                                                                          | -                       |
| `result.pagination.totalRecords` | `number`                                                                                                                                                          | -                       |
| `success`                        | `boolean`                                                                                                                                                         | Status of API response. |

#### Defined in

[socket-v2-sdk/src/client/models/ActiveRoutesOutputDTO.ts:3](https://github.com/rugamoto/socket-v2-sdk/blob/91d9fe3/src/client/models/ActiveRoutesOutputDTO.ts#L3)

---

### ApprovalData

Ƭ **ApprovalData**: `Object`

#### Type declaration

| Name                    | Type     | Description                                      |
| :---------------------- | :------- | :----------------------------------------------- |
| `allowanceTarget`       | `string` | Contract address that needs approval.            |
| `approvalTokenAddress`  | `string` | Address of token for which approval is required. |
| `minimumApprovalAmount` | `string` | Minimum amount of approval needed.               |
| `owner`                 | `string` | Address of owner.                                |

#### Defined in

[socket-v2-sdk/src/client/models/ApprovalData.ts:1](https://github.com/rugamoto/socket-v2-sdk/blob/91d9fe3/src/client/models/ApprovalData.ts#L1)

---

### ApprovalOutputDTO

Ƭ **ApprovalOutputDTO**: `Object`

#### Type declaration

| Name                  | Type                                             |
| :-------------------- | :----------------------------------------------- |
| `result`              | { `tokenAddress`: `string` ; `value`: `string` } |
| `result.tokenAddress` | `string`                                         |
| `result.value`        | `string`                                         |
| `success`             | `boolean`                                        |

#### Defined in

[socket-v2-sdk/src/client/models/ApprovalOutputDTO.ts:1](https://github.com/rugamoto/socket-v2-sdk/blob/91d9fe3/src/client/models/ApprovalOutputDTO.ts#L1)

---

### ApprovalTxOutputDTO

Ƭ **ApprovalTxOutputDTO**: `Object`

#### Type declaration

| Name           | Type                                                        |
| :------------- | :---------------------------------------------------------- |
| `result`       | { `data?`: `string` ; `from?`: `string` ; `to?`: `string` } |
| `result.data?` | `string`                                                    |
| `result.from?` | `string`                                                    |
| `result.to?`   | `string`                                                    |
| `success`      | `boolean`                                                   |

#### Defined in

[socket-v2-sdk/src/client/models/ApprovalTxOutputDTO.ts:1](https://github.com/rugamoto/socket-v2-sdk/blob/91d9fe3/src/client/models/ApprovalTxOutputDTO.ts#L1)

---

### Balance

Ƭ **Balance**: `Object`

#### Type declaration

| Name      | Type                                        |
| :-------- | :------------------------------------------ |
| `result`  | [`BalanceResult`](types.md#balanceresult)[] |
| `success` | `boolean`                                   |

#### Defined in

[socket-v2-sdk/src/client/models/Balance.ts:3](https://github.com/rugamoto/socket-v2-sdk/blob/91d9fe3/src/client/models/Balance.ts#L3)

---

### BalanceResult

Ƭ **BalanceResult**: `Object`

#### Type declaration

| Name       | Type                          |
| :--------- | :---------------------------- |
| `address`  | `string`                      |
| `amount`   | `number`                      |
| `chainId`  | [`ChainId`](enums/ChainId.md) |
| `currency` | `string`                      |
| `decimals` | `number`                      |
| `name`     | `string`                      |
| `price`    | `number`                      |
| `symbol`   | `string`                      |

#### Defined in

[socket-v2-sdk/src/client/models/BalanceResult.ts:3](https://github.com/rugamoto/socket-v2-sdk/blob/91d9fe3/src/client/models/BalanceResult.ts#L3)

---

### BridgeDetails

Ƭ **BridgeDetails**: `Object`

#### Type declaration

| Name          | Type                                | Description                          |
| :------------ | :---------------------------------- | :----------------------------------- |
| `displayName` | `string`                            | Display name of bridge.              |
| `icon?`       | `string`                            | URL for icon of bridge.              |
| `name`        | [`BridgeName`](enums/BridgeName.md) | Name of bridge.                      |
| `serviceTime` | `number`                            | Approx time for bridging in seconds. |

#### Defined in

[socket-v2-sdk/src/client/models/BridgeDetails.ts:5](https://github.com/rugamoto/socket-v2-sdk/blob/91d9fe3/src/client/models/BridgeDetails.ts#L5)

---

### BridgeRouteErrors

Ƭ **BridgeRouteErrors**: { [bridge in BridgeName]?: Object }

#### Defined in

[socket-v2-sdk/src/client/models/BridgeRouteErrors.ts:8](https://github.com/rugamoto/socket-v2-sdk/blob/91d9fe3/src/client/models/BridgeRouteErrors.ts#L8)

---

### BridgeStatusResponse

Ƭ **BridgeStatusResponse**: `Object`

#### Type declaration

| Name                          | Type                            | Description                                       |
| :---------------------------- | :------------------------------ | :------------------------------------------------ |
| `destinationTransactionHash?` | `string`                        | Destination Transaction hash.                     |
| `destinationTxStatus`         | [`TxStatus`](enums/TxStatus.md) | Status of destination transaction while bridging. |
| `fromChainId`                 | `number`                        | Source Chain Id                                   |
| `sourceTx`                    | `string`                        | Source Transaction.                               |
| `sourceTxStatus`              | [`TxStatus`](enums/TxStatus.md) | Status of source transaction while bridging.      |
| `toChainId`                   | `number`                        | Destination Chain Id.                             |

#### Defined in

[socket-v2-sdk/src/client/models/BridgeStatusResponse.ts:3](https://github.com/rugamoto/socket-v2-sdk/blob/91d9fe3/src/client/models/BridgeStatusResponse.ts#L3)

---

### BridgeStatusResponseDTO

Ƭ **BridgeStatusResponseDTO**: `Object`

#### Type declaration

| Name      | Type                                                    | Description    |
| :-------- | :------------------------------------------------------ | :------------- |
| `result`  | [`BridgeStatusResponse`](types.md#bridgestatusresponse) | -              |
| `success` | `boolean`                                               | Status of API. |

#### Defined in

[socket-v2-sdk/src/client/models/BridgeStatusResponseDTO.ts:3](https://github.com/rugamoto/socket-v2-sdk/blob/91d9fe3/src/client/models/BridgeStatusResponseDTO.ts#L3)

---

### ChainDetails

Ƭ **ChainDetails**: `Object`

#### Type declaration

| Name               | Type                                          | Description                                                        |
| :----------------- | :-------------------------------------------- | :----------------------------------------------------------------- |
| `chainId`          | [`ChainId`](enums/ChainId.md)                 | Id of chain.                                                       |
| `currency`         | [`GasTokenDetails`](types.md#gastokendetails) | -                                                                  |
| `explorers`        | `string`[]                                    | -                                                                  |
| `icon`             | `string`                                      | URL for icon of chain.                                             |
| `isL1`             | `boolean`                                     | Flag indicating whether the chain is L1.                           |
| `name`             | `string`                                      | Name of chain.                                                     |
| `receivingEnabled` | `boolean`                                     | Flag indicating whether receiving of tokens is supported to chain. |
| `rpcs`             | `string`[]                                    | -                                                                  |
| `sendingEnabled`   | `boolean`                                     | Flag indicating whether sending of tokens is supported from chain. |

#### Defined in

[socket-v2-sdk/src/client/models/ChainDetails.ts:4](https://github.com/rugamoto/socket-v2-sdk/blob/91d9fe3/src/client/models/ChainDetails.ts#L4)

---

### ChainGasBalances

Ƭ **ChainGasBalances**: `any`

#### Defined in

[socket-v2-sdk/src/client/models/ChainGasBalances.ts:1](https://github.com/rugamoto/socket-v2-sdk/blob/91d9fe3/src/client/models/ChainGasBalances.ts#L1)

---

### ChainSwitchDoneCallback

Ƭ **ChainSwitchDoneCallback**: (`chainId`: [`ChainId`](enums/ChainId.md)) => `void`

#### Type declaration

▸ (`chainId`): `void`

Callback when chain switch has completed.

##### Parameters

| Name      | Type                          |
| :-------- | :---------------------------- |
| `chainId` | [`ChainId`](enums/ChainId.md) |

##### Returns

`void`

#### Defined in

[socket-v2-sdk/src/web3ConnectedSocket.ts:26](https://github.com/rugamoto/socket-v2-sdk/blob/b3c3e8d/src/web3ConnectedSocket.ts#L26)

---

### Dexes

Ƭ **Dexes**: `Middleware.OneInch` \| `Middleware.ZeroX`

#### Defined in

[socket-v2-sdk/src/client/models/Dexes.ts:3](https://github.com/rugamoto/socket-v2-sdk/blob/91d9fe3/src/client/models/Dexes.ts#L3)

---

### GasFee

Ƭ **GasFee**: `Object`

#### Type declaration

| Name        | Type                      | Description                                 |
| :---------- | :------------------------ | :------------------------------------------ |
| `asset`     | [`Token`](types.md#token) | Gas token details.                          |
| `feesInUsd` | `number`                  | USD value of gas fees at current gas price. |
| `gasAmount` | `string`                  | Estimated Amount of gas token will be used  |
| `gasLimit`  | `number`                  | Approx Gas Limit of the transaction.        |

#### Defined in

[socket-v2-sdk/src/client/models/GasFee.ts:3](https://github.com/rugamoto/socket-v2-sdk/blob/91d9fe3/src/client/models/GasFee.ts#L3)

---

### GasPriceResponseDTO

Ƭ **GasPriceResponseDTO**: `Object`

#### Type declaration

| Name                              | Type                                                                                                                                                                                                                                                                                 |
| :-------------------------------- | :----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| `result`                          | { `chainId?`: [`ChainId`](enums/ChainId.md) ; `fast?`: { `estimatedSeconds?`: `number` ; `gasPrice?`: `number` } ; `normal?`: { `estimatedSeconds?`: `number` ; `gasPrice?`: `number` } ; `slow?`: { `estimatedSeconds?`: `number` ; `gasPrice?`: `number` } ; `txType?`: `number` } |
| `result.chainId?`                 | [`ChainId`](enums/ChainId.md)                                                                                                                                                                                                                                                        |
| `result.fast?`                    | { `estimatedSeconds?`: `number` ; `gasPrice?`: `number` }                                                                                                                                                                                                                            |
| `result.fast.estimatedSeconds?`   | `number`                                                                                                                                                                                                                                                                             |
| `result.fast.gasPrice?`           | `number`                                                                                                                                                                                                                                                                             |
| `result.normal?`                  | { `estimatedSeconds?`: `number` ; `gasPrice?`: `number` }                                                                                                                                                                                                                            |
| `result.normal.estimatedSeconds?` | `number`                                                                                                                                                                                                                                                                             |
| `result.normal.gasPrice?`         | `number`                                                                                                                                                                                                                                                                             |
| `result.slow?`                    | { `estimatedSeconds?`: `number` ; `gasPrice?`: `number` }                                                                                                                                                                                                                            |
| `result.slow.estimatedSeconds?`   | `number`                                                                                                                                                                                                                                                                             |
| `result.slow.gasPrice?`           | `number`                                                                                                                                                                                                                                                                             |
| `result.txType?`                  | `number`                                                                                                                                                                                                                                                                             |
| `success`                         | `boolean`                                                                                                                                                                                                                                                                            |

#### Defined in

[socket-v2-sdk/src/client/models/GasPriceResponseDTO.ts:3](https://github.com/rugamoto/socket-v2-sdk/blob/91d9fe3/src/client/models/GasPriceResponseDTO.ts#L3)

---

### GasTokenDetails

Ƭ **GasTokenDetails**: `Object`

#### Type declaration

| Name                      | Type     | Description                                               |
| :------------------------ | :------- | :-------------------------------------------------------- |
| `address`                 | `string` | Address of gas token.                                     |
| `decimals`                | `number` | Decimals of gas token.                                    |
| `icon`                    | `string` | URL for icon of gas token.                                |
| `minNativeCurrencyForGas` | `string` | Minimum amount to be left for gas while using max amount. |
| `name`                    | `string` | Name of gas token.                                        |
| `symbol`                  | `string` | Symbol of gas token.                                      |

#### Defined in

[socket-v2-sdk/src/client/models/GasTokenDetails.ts:1](https://github.com/rugamoto/socket-v2-sdk/blob/91d9fe3/src/client/models/GasTokenDetails.ts#L1)

---

### HealthResponseDTO

Ƭ **HealthResponseDTO**: `Object`

#### Type declaration

| Name | Type      |
| :--- | :-------- |
| `ok` | `boolean` |

#### Defined in

[socket-v2-sdk/src/client/models/HealthResponseDTO.ts:1](https://github.com/rugamoto/socket-v2-sdk/blob/91d9fe3/src/client/models/HealthResponseDTO.ts#L1)

---

### MinGasBalances

Ƭ **MinGasBalances**: `any`

#### Defined in

[socket-v2-sdk/src/client/models/MinGasBalances.ts:1](https://github.com/rugamoto/socket-v2-sdk/blob/91d9fe3/src/client/models/MinGasBalances.ts#L1)

---

### NextTxOutputDTO

Ƭ **NextTxOutputDTO**: `Object`

#### Type declaration

| Name     | Type                                             | Description    |
| :------- | :----------------------------------------------- | :------------- |
| `result` | [`NextTxResponse`](interfaces/NextTxResponse.md) | -              |
| `status` | `boolean`                                        | Status of API. |

#### Defined in

[socket-v2-sdk/src/client/models/NextTxOutputDTO.ts:3](https://github.com/rugamoto/socket-v2-sdk/blob/91d9fe3/src/client/models/NextTxOutputDTO.ts#L3)

---

### OpenAPIConfig

Ƭ **OpenAPIConfig**: `Object`

#### Type declaration

| Name               | Type                                       |
| :----------------- | :----------------------------------------- |
| `API_KEY?`         | `string` \| `Resolver`<`string`\>          |
| `BASE`             | `string`                                   |
| `CREDENTIALS`      | `"include"` \| `"omit"` \| `"same-origin"` |
| `HEADERS?`         | `Headers` \| `Resolver`<`Headers`\>        |
| `PASSWORD?`        | `string` \| `Resolver`<`string`\>          |
| `TOKEN?`           | `string` \| `Resolver`<`string`\>          |
| `USERNAME?`        | `string` \| `Resolver`<`string`\>          |
| `VERSION`          | `string`                                   |
| `WITH_CREDENTIALS` | `boolean`                                  |
| `ENCODE_PATH?`     | (`path`: `string`) => `string`             |

#### Defined in

[socket-v2-sdk/src/client/core/OpenAPI.ts:6](https://github.com/rugamoto/socket-v2-sdk/blob/91d9fe3/src/client/core/OpenAPI.ts#L6)

---

### Quote

Ƭ **Quote**: `Object`

#### Type declaration

| Name                | Type                                              |
| :------------------ | :------------------------------------------------ |
| `bridgeRouteErrors` | [`BridgeRouteErrors`](types.md#bridgerouteerrors) |
| `fromAsset?`        | [`Token`](types.md#token)                         |
| `fromChainId?`      | `number`                                          |
| `refuel?`           | [`RefuelData`](interfaces/RefuelData.md)          |
| `routes?`           | [`Route`](types.md#route)[]                       |
| `toAsset?`          | [`Token`](types.md#token)                         |
| `toChainId?`        | `number`                                          |

#### Defined in

[socket-v2-sdk/src/client/models/QuoteOutputDTO.ts:6](https://github.com/rugamoto/socket-v2-sdk/blob/91d9fe3/src/client/models/QuoteOutputDTO.ts#L6)

---

### QuoteOutputDTO

Ƭ **QuoteOutputDTO**: `Object`

#### Type declaration

| Name      | Type                      | Description    |
| :-------- | :------------------------ | :------------- |
| `result`  | [`Quote`](types.md#quote) | -              |
| `success` | `boolean`                 | Status of API. |

#### Defined in

[socket-v2-sdk/src/client/models/QuoteOutputDTO.ts:16](https://github.com/rugamoto/socket-v2-sdk/blob/91d9fe3/src/client/models/QuoteOutputDTO.ts#L16)

---

### Route

Ƭ **Route**: `Object`

#### Type declaration

| Name                 | Type                                            | Description                                                        |
| :------------------- | :---------------------------------------------- | :----------------------------------------------------------------- |
| `chainGasBalances`   | [`ChainGasBalances`](types.md#chaingasbalances) | -                                                                  |
| `fromAmount`         | `string`                                        | Sending token amount.                                              |
| `minimumGasBalances` | [`MinGasBalances`](types.md#mingasbalances)     | -                                                                  |
| `recipient`          | `string`                                        | Address of user receiving the amount.                              |
| `routeId`            | `string`                                        | Unique id for each route.                                          |
| `sender`             | `string`                                        | Address of user making the transactions.                           |
| `serviceTime`        | `number`                                        | Estimate of total time in seconds, excluding the transaction time. |
| `toAmount`           | `string`                                        | Approximate receiving token amount.                                |
| `totalGasFeesInUsd`  | `number`                                        | Combined USD gas fees for all transactions in the route.           |
| `totalUserTx`        | `number`                                        | Total number of transactions for the route.                        |
| `usedBridgeNames`    | [`BridgeName`](enums/BridgeName.md)[]           | Array of bridges used in the route                                 |
| `userTxs`            | [`UserTx`](types.md#usertx)[]                   | Array of user transactions.                                        |

#### Defined in

[socket-v2-sdk/src/client/models/Route.ts:6](https://github.com/rugamoto/socket-v2-sdk/blob/91d9fe3/src/client/models/Route.ts#L6)

---

### RouteStatusOutputDTO

Ƭ **RouteStatusOutputDTO**: `Object`

#### Type declaration

| Name     | Type                                                            | Description    |
| :------- | :-------------------------------------------------------------- | :------------- |
| `result` | [`PrepareActiveRouteStatus`](enums/PrepareActiveRouteStatus.md) | -              |
| `status` | `boolean`                                                       | Status of API. |

#### Defined in

[socket-v2-sdk/src/client/models/RouteStatusOutputDTO.ts:12](https://github.com/rugamoto/socket-v2-sdk/blob/91d9fe3/src/client/models/RouteStatusOutputDTO.ts#L12)

---

### SingleTxDTO

Ƭ **SingleTxDTO**: `Object`

#### Type declaration

| Name     | Type                                     |
| :------- | :--------------------------------------- |
| `refuel` | [`RefuelData`](interfaces/RefuelData.md) |
| `route`  | [`Route`](types.md#route)                |

#### Defined in

[socket-v2-sdk/src/client/models/SingleTxDTO.ts:4](https://github.com/rugamoto/socket-v2-sdk/blob/91d9fe3/src/client/models/SingleTxDTO.ts#L4)

---

### SingleTxOutputDTO

Ƭ **SingleTxOutputDTO**: `Object`

#### Type declaration

| Name     | Type                                            | Description    |
| :------- | :---------------------------------------------- | :------------- |
| `result` | [`SingleTxResponse`](types.md#singletxresponse) | -              |
| `status` | `boolean`                                       | Status of API. |

#### Defined in

[socket-v2-sdk/src/client/models/SingleTxOutputDTO.ts:3](https://github.com/rugamoto/socket-v2-sdk/blob/91d9fe3/src/client/models/SingleTxOutputDTO.ts#L3)

---

### SingleTxResponse

Ƭ **SingleTxResponse**: `Object`

#### Type declaration

| Name           | Type                                              | Description                                      |
| :------------- | :------------------------------------------------ | :----------------------------------------------- |
| `approvalData` | [`ApprovalData`](types.md#approvaldata) \| `null` | -                                                |
| `chainId`      | [`ChainId`](enums/ChainId.md)                     | Id of chain where transaction has to be sent.    |
| `totalUserTx`  | `number`                                          | Total number of transactions in Active Route.    |
| `txData`       | `string`                                          | Calldata for transaction.                        |
| `txTarget`     | `string`                                          | Address to which transaction has to be sent.     |
| `txType`       | [`TxType`](enums/TxType.md)                       | Type of transaction.                             |
| `userTxType`   | [`UserTxType`](enums/UserTxType.md)               | Type of user transaction.                        |
| `value`        | `string`                                          | Native token amount to be sent with transaction. |

#### Defined in

[socket-v2-sdk/src/client/models/SingleTxResponse.ts:6](https://github.com/rugamoto/socket-v2-sdk/blob/91d9fe3/src/client/models/SingleTxResponse.ts#L6)

---

### SocketTxDoneCallback

Ƭ **SocketTxDoneCallback**: (`tx`: [`SocketTx`](sdk/SocketTx.md)) => `void`

#### Type declaration

▸ (`tx`): `void`

Callback when a socket transaction is complete.

##### Parameters

| Name | Type                          |
| :--- | :---------------------------- |
| `tx` | [`SocketTx`](sdk/SocketTx.md) |

##### Returns

`void`

#### Defined in

[socket-v2-sdk/src/web3ConnectedSocket.ts:22](https://github.com/rugamoto/socket-v2-sdk/blob/b3c3e8d/src/web3ConnectedSocket.ts#L22)

---

### StartActiveRouteInputDTO

Ƭ **StartActiveRouteInputDTO**: `Object`

#### Type declaration

| Name                     | Type                                     | Description                                                                                                                                                                   |
| :----------------------- | :--------------------------------------- | :---------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| `fromAssetAddress`       | `string`                                 | Token address on source chain.                                                                                                                                                |
| `fromChainId`            | `number`                                 | Chain id of source chain.                                                                                                                                                     |
| `includeFirstTxDetails?` | `boolean`                                | Include the tx details for the first user transaction. If true it will return the txData txType etc. If false, it will only return the active route Id of the selected route. |
| `refuel?`                | [`RefuelData`](interfaces/RefuelData.md) | Refuel data for if the user have selected bridge with gas option                                                                                                              |
| `route`                  | [`Route`](types.md#route)                | Selected route by the user to bridge tokens from one chain to another.                                                                                                        |
| `toAssetAddress`         | `string`                                 | Token address on destination chain.                                                                                                                                           |
| `toChainId`              | `number`                                 | Chain id of destination chain.                                                                                                                                                |

#### Defined in

[socket-v2-sdk/src/client/models/StartActiveRouteInputDTO.ts:4](https://github.com/rugamoto/socket-v2-sdk/blob/91d9fe3/src/client/models/StartActiveRouteInputDTO.ts#L4)

---

### Step

Ƭ **Step**: `Object`

#### Type declaration

| Name          | Type                                      |
| :------------ | :---------------------------------------- |
| `fromAmount`  | `string`                                  |
| `fromAsset`   | [`Token`](types.md#token)                 |
| `fromChainId` | `number`                                  |
| `gasFees`     | [`GasFee`](types.md#gasfee)               |
| `protocol`    | [`BridgeDetails`](types.md#bridgedetails) |
| `serviceTime` | `number`                                  |
| `toAmount`    | `string`                                  |
| `toAsset`     | [`Token`](types.md#token)                 |
| `toChainId`   | `number`                                  |
| `type`        | `string`                                  |

#### Defined in

[socket-v2-sdk/src/client/models/UserTx.ts:9](https://github.com/rugamoto/socket-v2-sdk/blob/91d9fe3/src/client/models/UserTx.ts#L9)

---

### SupportedBridgesOutputDTO

Ƭ **SupportedBridgesOutputDTO**: `Object`

#### Type declaration

| Name      | Type                                        | Description    |
| :-------- | :------------------------------------------ | :------------- |
| `result`  | [`BridgeDetails`](types.md#bridgedetails)[] | -              |
| `success` | `boolean`                                   | Status of API. |

#### Defined in

[socket-v2-sdk/src/client/models/SupportedBridgesOutputDTO.ts:3](https://github.com/rugamoto/socket-v2-sdk/blob/91d9fe3/src/client/models/SupportedBridgesOutputDTO.ts#L3)

---

### SupportedChainsOutputDTO

Ƭ **SupportedChainsOutputDTO**: `Object`

#### Type declaration

| Name      | Type                                      | Description    |
| :-------- | :---------------------------------------- | :------------- |
| `result`  | [`ChainDetails`](types.md#chaindetails)[] | -              |
| `success` | `boolean`                                 | Status of API. |

#### Defined in

[socket-v2-sdk/src/client/models/SupportedChainsOutputDTO.ts:3](https://github.com/rugamoto/socket-v2-sdk/blob/91d9fe3/src/client/models/SupportedChainsOutputDTO.ts#L3)

---

### Token

Ƭ **Token**: `Object`

#### Type declaration

| Name               | Type                          | Description               |
| :----------------- | :---------------------------- | :------------------------ |
| `address`          | `string`                      | Address of token.         |
| `chainAgnosticId?` | `string` \| `null`            | Unique Id over all chains |
| `chainId`          | [`ChainId`](enums/ChainId.md) | Chain id of the token     |
| `decimals?`        | `number`                      | Decimal used for token.   |
| `icon?`            | `string`                      | URL for icon of token.    |
| `logoURI?`         | `string`                      | URL for icon of token.    |
| `name?`            | `string`                      | Name of token.            |
| `symbol`           | `string`                      | Symbol of token.          |

#### Defined in

[socket-v2-sdk/src/client/models/Token.ts:3](https://github.com/rugamoto/socket-v2-sdk/blob/91d9fe3/src/client/models/Token.ts#L3)

---

### TokenBalanceReponseDTO

Ƭ **TokenBalanceReponseDTO**: `Object`

#### Type declaration

| Name                   | Type                                                                                                                                                                                                              |
| :--------------------- | :---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| `result`               | { `balance?`: `string` ; `chainId?`: [`ChainId`](enums/ChainId.md) ; `decimals?`: `number` ; `icon?`: `string` ; `name?`: `string` ; `symbol?`: `string` ; `tokenAddress?`: `string` ; `userAddress?`: `string` } |
| `result.balance?`      | `string`                                                                                                                                                                                                          |
| `result.chainId?`      | [`ChainId`](enums/ChainId.md)                                                                                                                                                                                     |
| `result.decimals?`     | `number`                                                                                                                                                                                                          |
| `result.icon?`         | `string`                                                                                                                                                                                                          |
| `result.name?`         | `string`                                                                                                                                                                                                          |
| `result.symbol?`       | `string`                                                                                                                                                                                                          |
| `result.tokenAddress?` | `string`                                                                                                                                                                                                          |
| `result.userAddress?`  | `string`                                                                                                                                                                                                          |
| `success`              | `boolean`                                                                                                                                                                                                         |

#### Defined in

[socket-v2-sdk/src/client/models/TokenBalanceReponseDTO.ts:3](https://github.com/rugamoto/socket-v2-sdk/blob/91d9fe3/src/client/models/TokenBalanceReponseDTO.ts#L3)

---

### TokenListOutputDTO

Ƭ **TokenListOutputDTO**: `Object`

#### Type declaration

| Name      | Type                        | Description    |
| :-------- | :-------------------------- | :------------- |
| `result`  | [`Token`](types.md#token)[] | -              |
| `success` | `boolean`                   | Status of API. |

#### Defined in

[socket-v2-sdk/src/client/models/TokenListOutputDTO.ts:3](https://github.com/rugamoto/socket-v2-sdk/blob/91d9fe3/src/client/models/TokenListOutputDTO.ts#L3)

---

### TokenPriceResponseDTO

Ƭ **TokenPriceResponseDTO**: `Object`

#### Type declaration

| Name                   | Type                                                                                                                        |
| :--------------------- | :-------------------------------------------------------------------------------------------------------------------------- |
| `result`               | { `chainId?`: [`ChainId`](enums/ChainId.md) ; `currency?`: `string` ; `tokenAddress?`: `string` ; `tokenPrice?`: `number` } |
| `result.chainId?`      | [`ChainId`](enums/ChainId.md)                                                                                               |
| `result.currency?`     | `string`                                                                                                                    |
| `result.tokenAddress?` | `string`                                                                                                                    |
| `result.tokenPrice?`   | `number`                                                                                                                    |
| `success`              | `boolean`                                                                                                                   |

#### Defined in

[socket-v2-sdk/src/client/models/TokenPriceResponseDTO.ts:3](https://github.com/rugamoto/socket-v2-sdk/blob/91d9fe3/src/client/models/TokenPriceResponseDTO.ts#L3)

---

### TransactionReceiptResponseDTO

Ƭ **TransactionReceiptResponseDTO**: `Object`

#### Type declaration

| Name      | Type      | Description    |
| :-------- | :-------- | :------------- |
| `result`  | `any`     | -              |
| `success` | `boolean` | Status of API. |

#### Defined in

[socket-v2-sdk/src/client/models/TransactionReceiptResponseDTO.ts:1](https://github.com/rugamoto/socket-v2-sdk/blob/91d9fe3/src/client/models/TransactionReceiptResponseDTO.ts#L1)

---

### TxDoneCallback

Ƭ **TxDoneCallback**: (`tx`: [`SocketTx`](sdk/SocketTx.md), `hash`: `string`) => `void`

#### Type declaration

▸ (`tx`, `hash`): `void`

Callback when a transaction for send/approval has completed.

##### Parameters

| Name   | Type                          |
| :----- | :---------------------------- |
| `tx`   | [`SocketTx`](sdk/SocketTx.md) |
| `hash` | `string`                      |

##### Returns

`void`

#### Defined in

[socket-v2-sdk/src/web3ConnectedSocket.ts:24](https://github.com/rugamoto/socket-v2-sdk/blob/b3c3e8d/src/web3ConnectedSocket.ts#L24)

---

### UserTx

Ƭ **UserTx**: `Object`

#### Type declaration

| Name                        | Type                                                            |
| :-------------------------- | :-------------------------------------------------------------- |
| `approvalData?`             | [`ApprovalData`](types.md#approvaldata)                         |
| `chainId`                   | [`ChainId`](enums/ChainId.md)                                   |
| `destinationTxHash?`        | `string`                                                        |
| `destinationTxReceipt?`     | `TransactionReceipt`                                            |
| `gasFees`                   | [`GasFee`](types.md#gasfee)                                     |
| `recipient`                 | `string`                                                        |
| `routePath`                 | `string`                                                        |
| `sender`                    | `string`                                                        |
| `serviceTime`               | `number`                                                        |
| `sourceTransactionHash?`    | `string`                                                        |
| `sourceTransactionReceipt?` | `TransactionReceipt`                                            |
| `stepCount`                 | `number`                                                        |
| `steps`                     | [`Step`](types.md#step)[]                                       |
| `toAmount`                  | `string`                                                        |
| `toAsset`                   | [`Token`](types.md#token)                                       |
| `txType`                    | [`TxType`](enums/TxType.md)                                     |
| `userTxIndex`               | `number`                                                        |
| `userTxStatus?`             | [`PrepareActiveRouteStatus`](enums/PrepareActiveRouteStatus.md) |
| `userTxType`                | [`UserTxType`](enums/UserTxType.md)                             |

#### Defined in

[socket-v2-sdk/src/client/models/UserTx.ts:22](https://github.com/rugamoto/socket-v2-sdk/blob/91d9fe3/src/client/models/UserTx.ts#L22)

## Variables

### OpenAPI

• `Const` **OpenAPI**: [`OpenAPIConfig`](types.md#openapiconfig)

#### Defined in

[socket-v2-sdk/src/client/core/OpenAPI.ts:19](https://github.com/rugamoto/socket-v2-sdk/blob/91d9fe3/src/client/core/OpenAPI.ts#L19)

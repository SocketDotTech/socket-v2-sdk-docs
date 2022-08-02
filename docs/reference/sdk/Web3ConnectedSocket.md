---
sidebar_position: 2
---

# Web3ConnectedSocket

The Socket represents the socket sdk. This is the starting point for interacting with the socket SDK. It allows you to retrieve routes and start the execution of trades based on quotes

It includes direct access to the socket api.

The connected socket sdk interfaces directly with wallets

## Hierarchy

- `BaseSocket`

  ↳ **`Web3ConnectedSocket`**

## Table of contents

### Constructors

- [constructor](Web3ConnectedSocket.md#constructor)

### Properties

- [\_provider](Web3ConnectedSocket.md#_provider)
- [client](Web3ConnectedSocket.md#client)

### Methods

- [continue](Web3ConnectedSocket.md#continue)
- [getActiveRoutes](Web3ConnectedSocket.md#getactiveroutes)
- [getAllQuotes](Web3ConnectedSocket.md#getallquotes)
- [getBestQuote](Web3ConnectedSocket.md#getbestquote)
- [getChain](Web3ConnectedSocket.md#getchain)
- [getChains](Web3ConnectedSocket.md#getchains)
- [getTokenList](Web3ConnectedSocket.md#gettokenlist)
- [start](Web3ConnectedSocket.md#start)

## Constructors

### constructor

• **new Web3ConnectedSocket**(`options`, `provider`)

#### Parameters

| Name       | Type                                              |
| :--------- | :------------------------------------------------ |
| `options`  | [`SocketOptions`](../interfaces/SocketOptions.md) |
| `provider` | `Web3Provider`                                    |

#### Overrides

BaseSocket.constructor

#### Defined in

[socket-v2-sdk/src/web3ConnectedSocket.ts:41](https://github.com/rugamoto/socket-v2-sdk/blob/b3c3e8d/src/web3ConnectedSocket.ts#L41)

## Properties

### \_provider

• `Readonly` **\_provider**: `Web3Provider`

#### Overrides

BaseSocket.\_provider

#### Defined in

[socket-v2-sdk/src/web3ConnectedSocket.ts:39](https://github.com/rugamoto/socket-v2-sdk/blob/b3c3e8d/src/web3ConnectedSocket.ts#L39)

---

### client

• **client**: `Object`

API client for accessing the socket api directly

#### Type declaration

| Name         | Type                                        |
| :----------- | :------------------------------------------ |
| `approvals`  | typeof [`Approvals`](../api/Approvals.md)   |
| `balances`   | typeof [`Balances`](../api/Balances.md)     |
| `quotes`     | typeof [`Quotes`](../api/Quotes.md)         |
| `routes`     | typeof [`Routes`](../api/Routes.md)         |
| `server`     | typeof [`Server`](../api/Server.md)         |
| `supported`  | typeof [`Supported`](../api/Supported.md)   |
| `tokenLists` | typeof [`TokenLists`](../api/TokenLists.md) |

#### Inherited from

BaseSocket.client

#### Defined in

[socket-v2-sdk/src/baseSocket.ts:54](https://github.com/rugamoto/socket-v2-sdk/blob/b3c3e8d/src/baseSocket.ts#L54)

## Methods

### continue

▸ **continue**(`activeRouteId`, `callbacks`): `Promise`<`void`\>

Continue an active route

#### Parameters

| Name            | Type                                                | Description                                              |
| :-------------- | :-------------------------------------------------- | :------------------------------------------------------- |
| `activeRouteId` | `number`                                            | The active route id of the desired route to continue     |
| `callbacks`     | [`EventCallbacks`](../interfaces/EventCallbacks.md) | optional callbacks for different states of the execution |

#### Returns

`Promise`<`void`\>

#### Defined in

[socket-v2-sdk/src/web3ConnectedSocket.ts:141](https://github.com/rugamoto/socket-v2-sdk/blob/b3c3e8d/src/web3ConnectedSocket.ts#L141)

---

### getActiveRoutes

▸ **getActiveRoutes**(`options`): `Promise`<{ `activeRoutes`: [`ActiveRouteResponse`](../types.md#activerouteresponse)[] ; `pagination`: { `limit`: `number` ; `offset`: `number` ; `totalRecords`: `number` } }\>

Retrieve the active routes. Active routes can be used to continue a quote

#### Parameters

| Name      | Type                                                          | Description                                                             |
| :-------- | :------------------------------------------------------------ | :---------------------------------------------------------------------- |
| `options` | [`ActiveRoutesRequest`](../interfaces/ActiveRoutesRequest.md) | Criteria for returning active routes. Commonly `address` is most useful |

#### Returns

`Promise`<{ `activeRoutes`: [`ActiveRouteResponse`](../types.md#activerouteresponse)[] ; `pagination`: { `limit`: `number` ; `offset`: `number` ; `totalRecords`: `number` } }\>

list of active routes

#### Inherited from

BaseSocket.getActiveRoutes

#### Defined in

[socket-v2-sdk/src/baseSocket.ts:201](https://github.com/rugamoto/socket-v2-sdk/blob/b3c3e8d/src/baseSocket.ts#L201)

---

### getAllQuotes

▸ **getAllQuotes**(`params`, `preferences?`): `Promise`<[`SocketQuote`](../interfaces/SocketQuote.md)[]\>

Get All quotes

#### Parameters

| Name           | Type                                                    | Description                                                        |
| :------------- | :------------------------------------------------------ | :----------------------------------------------------------------- |
| `params`       | [`QuoteParams`](../interfaces/QuoteParams.md)           | The parameters of the quote                                        |
| `preferences?` | [`QuotePreferences`](../interfaces/QuotePreferences.md) | Additional route preferences for retrieving the quote from the api |

#### Returns

`Promise`<[`SocketQuote`](../interfaces/SocketQuote.md)[]\>

All quotes found

#### Inherited from

BaseSocket.getAllQuotes

#### Defined in

[socket-v2-sdk/src/baseSocket.ts:161](https://github.com/rugamoto/socket-v2-sdk/blob/b3c3e8d/src/baseSocket.ts#L161)

---

### getBestQuote

▸ **getBestQuote**(`params`, `preferences?`): `Promise`<`null` \| [`SocketQuote`](../interfaces/SocketQuote.md)\>

Get the best quote

#### Parameters

| Name           | Type                                                    | Description                                                        |
| :------------- | :------------------------------------------------------ | :----------------------------------------------------------------- |
| `params`       | [`QuoteParams`](../interfaces/QuoteParams.md)           | The parameters of the quote                                        |
| `preferences?` | [`QuotePreferences`](../interfaces/QuotePreferences.md) | Additional route preferences for retrieving the quote from the api |

#### Returns

`Promise`<`null` \| [`SocketQuote`](../interfaces/SocketQuote.md)\>

The best quote if found or null

#### Inherited from

BaseSocket.getBestQuote

#### Defined in

[socket-v2-sdk/src/baseSocket.ts:150](https://github.com/rugamoto/socket-v2-sdk/blob/b3c3e8d/src/baseSocket.ts#L150)

---

### getChain

▸ **getChain**(`chainId`): `Promise`<[`Chain`](Chain.md)\>

Get a chain by id

#### Parameters

| Name      | Type                             | Description                 |
| :-------- | :------------------------------- | :-------------------------- |
| `chainId` | [`ChainId`](../enums/ChainId.md) | The numeric id of the chain |

#### Returns

`Promise`<[`Chain`](Chain.md)\>

The requested chain

#### Inherited from

BaseSocket.getChain

#### Defined in

[socket-v2-sdk/src/baseSocket.ts:92](https://github.com/rugamoto/socket-v2-sdk/blob/b3c3e8d/src/baseSocket.ts#L92)

---

### getChains

▸ **getChains**(): `Promise`<[`Chain`](Chain.md)[]\>

Get all supported chains

#### Returns

`Promise`<[`Chain`](Chain.md)[]\>

List of chains

#### Inherited from

BaseSocket.getChains

#### Defined in

[socket-v2-sdk/src/baseSocket.ts:77](https://github.com/rugamoto/socket-v2-sdk/blob/b3c3e8d/src/baseSocket.ts#L77)

---

### getTokenList

▸ **getTokenList**(`request`): `Promise`<{ `from`: [`TokenList`](TokenList.md) ; `to`: [`TokenList`](TokenList.md) }\>

Get the list of tokens available for each chain for a given path

#### Parameters

| Name      | Type                                                    |
| :-------- | :------------------------------------------------------ |
| `request` | [`TokenListRequest`](../interfaces/TokenListRequest.md) |

#### Returns

`Promise`<{ `from`: [`TokenList`](TokenList.md) ; `to`: [`TokenList`](TokenList.md) }\>

The `from` and `to` token lists

#### Inherited from

BaseSocket.getTokenList

#### Defined in

[socket-v2-sdk/src/baseSocket.ts:110](https://github.com/rugamoto/socket-v2-sdk/blob/b3c3e8d/src/baseSocket.ts#L110)

---

### start

▸ **start**(`quote`, `callbacks`): `Promise`<`number`\>

Start executing the quote on the provider

#### Parameters

| Name        | Type                                                | Description                                              |
| :---------- | :-------------------------------------------------- | :------------------------------------------------------- |
| `quote`     | [`SocketQuote`](../interfaces/SocketQuote.md)       | The quote to execute                                     |
| `callbacks` | [`EventCallbacks`](../interfaces/EventCallbacks.md) | optional callbacks for different states of the execution |

#### Returns

`Promise`<`number`\>

#### Defined in

[socket-v2-sdk/src/web3ConnectedSocket.ts:130](https://github.com/rugamoto/socket-v2-sdk/blob/b3c3e8d/src/web3ConnectedSocket.ts#L130)

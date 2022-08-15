---
sidebar_position: 1
---

# Socket

The Socket represents the socket sdk. This is the starting point for interacting with the socket SDK. It allows you to retrieve routes and start the execution of trades based on quotes

It includes direct access to the socket api.

## Hierarchy

- `BaseSocket`

  ↳ **`Socket`**

## Table of contents

### Constructors

- [constructor](Socket.md#constructor)

### Properties

- [client](Socket.md#client)

### Methods

- [connect](Socket.md#connect)
- [continue](Socket.md#continue)
- [getActiveRoutes](Socket.md#getactiveroutes)
- [getAllQuotes](Socket.md#getallquotes)
- [getBestQuote](Socket.md#getbestquote)
- [getChain](Socket.md#getchain)
- [getChains](Socket.md#getchains)
- [getTokenList](Socket.md#gettokenlist)
- [start](Socket.md#start)

## Constructors

### constructor

• **new Socket**(`options`)

#### Parameters

| Name      | Type                                              | Description        |
| :-------- | :------------------------------------------------ | :----------------- |
| `options` | [`SocketOptions`](../interfaces/SocketOptions.md) | Socket sdk options |

#### Inherited from

BaseSocket.constructor

#### Defined in

[socket-v2-sdk/src/baseSocket.ts:68](https://github.com/SocketDotTech/socket-v2-sdk/blob/b3c3e8d/src/baseSocket.ts#L68)

## Properties

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

[socket-v2-sdk/src/baseSocket.ts:54](https://github.com/SocketDotTech/socket-v2-sdk/blob/b3c3e8d/src/baseSocket.ts#L54)

## Methods

### connect

▸ **connect**(`provider`): [`Web3ConnectedSocket`](Web3ConnectedSocket.md)

Connect Socket to a web3 provider that will be used to execute routes

#### Parameters

| Name       | Type           | Description                             |
| :--------- | :------------- | :-------------------------------------- |
| `provider` | `Web3Provider` | The web3 provider to use as user wallet |

#### Returns

[`Web3ConnectedSocket`](Web3ConnectedSocket.md)

#### Defined in

[socket-v2-sdk/src/socket.ts:31](https://github.com/SocketDotTech/socket-v2-sdk/blob/b3c3e8d/src/socket.ts#L31)

---

### continue

▸ **continue**(`activeRouteId`): `Promise`<`ActiveRouteGenerator`\>

Continue an active route

#### Parameters

| Name            | Type     | Description                                          |
| :-------------- | :------- | :--------------------------------------------------- |
| `activeRouteId` | `number` | The active route id of the desired route to continue |

#### Returns

`Promise`<`ActiveRouteGenerator`\>

An iterator that will yield each transaction required in the route

#### Defined in

[socket-v2-sdk/src/socket.ts:23](https://github.com/SocketDotTech/socket-v2-sdk/blob/b3c3e8d/src/socket.ts#L23)

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

[socket-v2-sdk/src/baseSocket.ts:201](https://github.com/SocketDotTech/socket-v2-sdk/blob/b3c3e8d/src/baseSocket.ts#L201)

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

[socket-v2-sdk/src/baseSocket.ts:161](https://github.com/SocketDotTech/socket-v2-sdk/blob/b3c3e8d/src/baseSocket.ts#L161)

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

[socket-v2-sdk/src/baseSocket.ts:150](https://github.com/SocketDotTech/socket-v2-sdk/blob/b3c3e8d/src/baseSocket.ts#L150)

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

[socket-v2-sdk/src/baseSocket.ts:92](https://github.com/SocketDotTech/socket-v2-sdk/blob/b3c3e8d/src/baseSocket.ts#L92)

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

[socket-v2-sdk/src/baseSocket.ts:77](https://github.com/SocketDotTech/socket-v2-sdk/blob/b3c3e8d/src/baseSocket.ts#L77)

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

[socket-v2-sdk/src/baseSocket.ts:110](https://github.com/SocketDotTech/socket-v2-sdk/blob/b3c3e8d/src/baseSocket.ts#L110)

---

### start

▸ **start**(`quote`): `Promise`<`ActiveRouteGenerator`\>

Start executing a socket quote/route.

#### Parameters

| Name    | Type                                          |
| :------ | :-------------------------------------------- |
| `quote` | [`SocketQuote`](../interfaces/SocketQuote.md) |

#### Returns

`Promise`<`ActiveRouteGenerator`\>

An iterator that will yield each transaction required in the route

#### Defined in

[socket-v2-sdk/src/socket.ts:14](https://github.com/SocketDotTech/socket-v2-sdk/blob/b3c3e8d/src/socket.ts#L14)

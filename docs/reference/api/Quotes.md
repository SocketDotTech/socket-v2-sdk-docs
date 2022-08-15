# Quotes

## Table of contents

### Constructors

- [constructor](Quotes.md#constructor)

### Methods

- [getQuote](Quotes.md#getquote)

## Constructors

### constructor

• **new Quotes**()

## Methods

### getQuote

▸ `Static` **getQuote**(`quoteRequest`): [`CancelablePromise`](../client/CancelablePromise.md)<[`QuoteOutputDTO`](../types.md#quoteoutputdto)\>

**`throws`** ApiError

#### Parameters

| Name           | Type                                            |
| :------------- | :---------------------------------------------- |
| `quoteRequest` | [`QuoteRequest`](../interfaces/QuoteRequest.md) |

#### Returns

[`CancelablePromise`](../client/CancelablePromise.md)<[`QuoteOutputDTO`](../types.md#quoteoutputdto)\>

QuoteOutputDTO Returns all the possible routes for bridging tokens from one chain to another. One of the routes can be selected and passed in to start the route.

#### Defined in

[socket-v2-sdk/src/client/services/Quote.ts:13](https://github.com/SocketDotTech/socket-v2-sdk/blob/91d9fe3/src/client/services/Quote.ts#L13)

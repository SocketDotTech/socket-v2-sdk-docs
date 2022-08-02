# SocketQuote

Quote parameters and the retrieved route

## Hierarchy

- [`QuoteParams`](QuoteParams.md)

  ↳ **`SocketQuote`**

## Table of contents

### Properties

- [address](SocketQuote.md#address)
- [amount](SocketQuote.md#amount)
- [errors](SocketQuote.md#errors)
- [path](SocketQuote.md#path)
- [refuel](SocketQuote.md#refuel)
- [route](SocketQuote.md#route)

## Properties

### address

• **address**: `string`

User address

#### Inherited from

[QuoteParams](QuoteParams.md).[address](QuoteParams.md#address)

#### Defined in

[socket-v2-sdk/src/types.ts:16](https://github.com/rugamoto/socket-v2-sdk/blob/91d9fe3/src/types.ts#L16)

---

### amount

• **amount**: `string`

Amount of the quote

#### Inherited from

[QuoteParams](QuoteParams.md).[amount](QuoteParams.md#amount)

#### Defined in

[socket-v2-sdk/src/types.ts:14](https://github.com/rugamoto/socket-v2-sdk/blob/91d9fe3/src/types.ts#L14)

---

### errors

• **errors**: [`BridgeRouteErrors`](../types.md#bridgerouteerrors)

Errors

#### Defined in

[socket-v2-sdk/src/types.ts:28](https://github.com/rugamoto/socket-v2-sdk/blob/91d9fe3/src/types.ts#L28)

---

### path

• **path**: [`Path`](../sdk/Path.md)

The path desired

#### Inherited from

[QuoteParams](QuoteParams.md).[path](QuoteParams.md#path)

#### Defined in

[socket-v2-sdk/src/types.ts:12](https://github.com/rugamoto/socket-v2-sdk/blob/91d9fe3/src/types.ts#L12)

---

### refuel

• `Optional` **refuel**: [`RefuelData`](RefuelData.md)

Refuel Data

#### Defined in

[socket-v2-sdk/src/types.ts:26](https://github.com/rugamoto/socket-v2-sdk/blob/91d9fe3/src/types.ts#L26)

---

### route

• **route**: [`Route`](../types.md#route)

The route retrieved for the quote

#### Defined in

[socket-v2-sdk/src/types.ts:24](https://github.com/rugamoto/socket-v2-sdk/blob/91d9fe3/src/types.ts#L24)

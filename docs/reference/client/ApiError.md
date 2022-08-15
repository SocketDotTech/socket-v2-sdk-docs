# ApiError

## Hierarchy

- `Error`

  ↳ **`ApiError`**

## Table of contents

### Constructors

- [constructor](ApiError.md#constructor)

### Properties

- [body](ApiError.md#body)
- [message](ApiError.md#message)
- [name](ApiError.md#name)
- [stack](ApiError.md#stack)
- [status](ApiError.md#status)
- [statusText](ApiError.md#statustext)
- [url](ApiError.md#url)
- [prepareStackTrace](ApiError.md#preparestacktrace)
- [stackTraceLimit](ApiError.md#stacktracelimit)

### Methods

- [captureStackTrace](ApiError.md#capturestacktrace)

## Constructors

### constructor

• **new ApiError**(`response`, `message`)

#### Parameters

| Name       | Type        |
| :--------- | :---------- |
| `response` | `ApiResult` |
| `message`  | `string`    |

#### Overrides

Error.constructor

#### Defined in

[src/client/core/ApiError.ts:9](https://github.com/SocketDotTech/socket-v2-sdk/blob/72e8f92/src/client/core/ApiError.ts#L9)

## Properties

### body

• `Readonly` **body**: `any`

#### Defined in

[src/client/core/ApiError.ts:7](https://github.com/SocketDotTech/socket-v2-sdk/blob/72e8f92/src/client/core/ApiError.ts#L7)

---

### message

• **message**: `string`

#### Inherited from

Error.message

#### Defined in

node_modules/typescript/lib/lib.es5.d.ts:1023

---

### name

• **name**: `string`

#### Inherited from

Error.name

#### Defined in

node_modules/typescript/lib/lib.es5.d.ts:1022

---

### stack

• `Optional` **stack**: `string`

#### Inherited from

Error.stack

#### Defined in

node_modules/typescript/lib/lib.es5.d.ts:1024

---

### status

• `Readonly` **status**: `number`

#### Defined in

[src/client/core/ApiError.ts:5](https://github.com/SocketDotTech/socket-v2-sdk/blob/72e8f92/src/client/core/ApiError.ts#L5)

---

### statusText

• `Readonly` **statusText**: `string`

#### Defined in

[src/client/core/ApiError.ts:6](https://github.com/SocketDotTech/socket-v2-sdk/blob/72e8f92/src/client/core/ApiError.ts#L6)

---

### url

• `Readonly` **url**: `string`

#### Defined in

[src/client/core/ApiError.ts:4](https://github.com/SocketDotTech/socket-v2-sdk/blob/72e8f92/src/client/core/ApiError.ts#L4)

---

### prepareStackTrace

▪ `Static` `Optional` **prepareStackTrace**: (`err`: `Error`, `stackTraces`: `CallSite`[]) => `any`

#### Type declaration

▸ (`err`, `stackTraces`): `any`

Optional override for formatting stack traces

**`see`** https://v8.dev/docs/stack-trace-api#customizing-stack-traces

##### Parameters

| Name          | Type         |
| :------------ | :----------- |
| `err`         | `Error`      |
| `stackTraces` | `CallSite`[] |

##### Returns

`any`

#### Inherited from

Error.prepareStackTrace

#### Defined in

node_modules/@types/node/globals.d.ts:11

---

### stackTraceLimit

▪ `Static` **stackTraceLimit**: `number`

#### Inherited from

Error.stackTraceLimit

#### Defined in

node_modules/@types/node/globals.d.ts:13

## Methods

### captureStackTrace

▸ `Static` **captureStackTrace**(`targetObject`, `constructorOpt?`): `void`

Create .stack property on a target object

#### Parameters

| Name              | Type       |
| :---------------- | :--------- |
| `targetObject`    | `object`   |
| `constructorOpt?` | `Function` |

#### Returns

`void`

#### Inherited from

Error.captureStackTrace

#### Defined in

node_modules/@types/node/globals.d.ts:4

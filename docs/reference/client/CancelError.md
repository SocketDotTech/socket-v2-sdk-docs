# CancelError

## Hierarchy

- `Error`

  ↳ **`CancelError`**

## Table of contents

### Constructors

- [constructor](CancelError.md#constructor)

### Properties

- [message](CancelError.md#message)
- [name](CancelError.md#name)
- [stack](CancelError.md#stack)
- [prepareStackTrace](CancelError.md#preparestacktrace)
- [stackTraceLimit](CancelError.md#stacktracelimit)

### Accessors

- [isCancelled](CancelError.md#iscancelled)

### Methods

- [captureStackTrace](CancelError.md#capturestacktrace)

## Constructors

### constructor

• **new CancelError**(`message`)

#### Parameters

| Name      | Type     |
| :-------- | :------- |
| `message` | `string` |

#### Overrides

Error.constructor

#### Defined in

[src/client/core/CancelablePromise.ts:2](https://github.com/SocketDotTech/socket-v2-sdk/blob/72e8f92/src/client/core/CancelablePromise.ts#L2)

## Properties

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

## Accessors

### isCancelled

• `get` **isCancelled**(): `boolean`

#### Returns

`boolean`

#### Defined in

[src/client/core/CancelablePromise.ts:7](https://github.com/SocketDotTech/socket-v2-sdk/blob/72e8f92/src/client/core/CancelablePromise.ts#L7)

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

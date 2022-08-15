# CancelablePromise<T\>

## Type parameters

| Name |
| :--- |
| `T`  |

## Implements

- `Promise`<`T`\>

## Table of contents

### Constructors

- [constructor](../client/CancelablePromise.md#constructor)

### Properties

- [[toStringTag]](../client/CancelablePromise.md#[tostringtag])
- [\_cancelHandlers](../client/CancelablePromise.md#_cancelhandlers)
- [\_isCancelled](../client/CancelablePromise.md#_iscancelled)
- [\_isRejected](../client/CancelablePromise.md#_isrejected)
- [\_isResolved](../client/CancelablePromise.md#_isresolved)
- [\_promise](../client/CancelablePromise.md#_promise)
- [\_reject](../client/CancelablePromise.md#_reject)
- [\_resolve](../client/CancelablePromise.md#_resolve)

### Accessors

- [isCancelled](../client/CancelablePromise.md#iscancelled)

### Methods

- [cancel](../client/CancelablePromise.md#cancel)
- [catch](../client/CancelablePromise.md#catch)
- [finally](../client/CancelablePromise.md#finally)
- [then](../client/CancelablePromise.md#then)

## Constructors

### constructor

• **new CancelablePromise**<`T`\>(`executor`)

#### Type parameters

| Name |
| :--- |
| `T`  |

#### Parameters

| Name       | Type                                                                                                                                   |
| :--------- | :------------------------------------------------------------------------------------------------------------------------------------- |
| `executor` | (`resolve`: (`value`: `T` \| `PromiseLike`<`T`\>) => `void`, `reject`: (`reason?`: `any`) => `void`, `onCancel`: `OnCancel`) => `void` |

#### Defined in

[src/client/core/CancelablePromise.ts:31](https://github.com/SocketDotTech/socket-v2-sdk/blob/72e8f92/src/client/core/CancelablePromise.ts#L31)

## Properties

### [toStringTag]

• `Readonly` **[toStringTag]**: `string`

#### Implementation of

Promise.\_\_@toStringTag@26

#### Defined in

[src/client/core/CancelablePromise.ts:21](https://github.com/SocketDotTech/socket-v2-sdk/blob/72e8f92/src/client/core/CancelablePromise.ts#L21)

---

### \_cancelHandlers

• `Private` `Readonly` **\_cancelHandlers**: () => `void`[]

#### Defined in

[src/client/core/CancelablePromise.ts:26](https://github.com/SocketDotTech/socket-v2-sdk/blob/72e8f92/src/client/core/CancelablePromise.ts#L26)

---

### \_isCancelled

• `Private` **\_isCancelled**: `boolean`

#### Defined in

[src/client/core/CancelablePromise.ts:25](https://github.com/SocketDotTech/socket-v2-sdk/blob/72e8f92/src/client/core/CancelablePromise.ts#L25)

---

### \_isRejected

• `Private` **\_isRejected**: `boolean`

#### Defined in

[src/client/core/CancelablePromise.ts:24](https://github.com/SocketDotTech/socket-v2-sdk/blob/72e8f92/src/client/core/CancelablePromise.ts#L24)

---

### \_isResolved

• `Private` **\_isResolved**: `boolean`

#### Defined in

[src/client/core/CancelablePromise.ts:23](https://github.com/SocketDotTech/socket-v2-sdk/blob/72e8f92/src/client/core/CancelablePromise.ts#L23)

---

### \_promise

• `Private` `Readonly` **\_promise**: `Promise`<`T`\>

#### Defined in

[src/client/core/CancelablePromise.ts:27](https://github.com/SocketDotTech/socket-v2-sdk/blob/72e8f92/src/client/core/CancelablePromise.ts#L27)

---

### \_reject

• `Private` `Optional` **\_reject**: (`reason?`: `any`) => `void`

#### Type declaration

▸ (`reason?`): `void`

##### Parameters

| Name      | Type  |
| :-------- | :---- |
| `reason?` | `any` |

##### Returns

`void`

#### Defined in

[src/client/core/CancelablePromise.ts:29](https://github.com/SocketDotTech/socket-v2-sdk/blob/72e8f92/src/client/core/CancelablePromise.ts#L29)

---

### \_resolve

• `Private` `Optional` **\_resolve**: (`value`: `T` \| `PromiseLike`<`T`\>) => `void`

#### Type declaration

▸ (`value`): `void`

##### Parameters

| Name    | Type                       |
| :------ | :------------------------- |
| `value` | `T` \| `PromiseLike`<`T`\> |

##### Returns

`void`

#### Defined in

[src/client/core/CancelablePromise.ts:28](https://github.com/SocketDotTech/socket-v2-sdk/blob/72e8f92/src/client/core/CancelablePromise.ts#L28)

## Accessors

### isCancelled

• `get` **isCancelled**(): `boolean`

#### Returns

`boolean`

#### Defined in

[src/client/core/CancelablePromise.ts:121](https://github.com/SocketDotTech/socket-v2-sdk/blob/72e8f92/src/client/core/CancelablePromise.ts#L121)

## Methods

### cancel

▸ **cancel**(): `void`

#### Returns

`void`

#### Defined in

[src/client/core/CancelablePromise.ts:102](https://github.com/SocketDotTech/socket-v2-sdk/blob/72e8f92/src/client/core/CancelablePromise.ts#L102)

---

### catch

▸ **catch**<`TResult`\>(`onRejected?`): `Promise`<`T` \| `TResult`\>

#### Type parameters

| Name      | Type    |
| :-------- | :------ |
| `TResult` | `never` |

#### Parameters

| Name          | Type                                                                  |
| :------------ | :-------------------------------------------------------------------- |
| `onRejected?` | `null` \| (`reason`: `any`) => `TResult` \| `PromiseLike`<`TResult`\> |

#### Returns

`Promise`<`T` \| `TResult`\>

#### Implementation of

Promise.catch

#### Defined in

[src/client/core/CancelablePromise.ts:92](https://github.com/SocketDotTech/socket-v2-sdk/blob/72e8f92/src/client/core/CancelablePromise.ts#L92)

---

### finally

▸ **finally**(`onFinally?`): `Promise`<`T`\>

#### Parameters

| Name         | Type                   |
| :----------- | :--------------------- |
| `onFinally?` | `null` \| () => `void` |

#### Returns

`Promise`<`T`\>

#### Implementation of

Promise.finally

#### Defined in

[src/client/core/CancelablePromise.ts:98](https://github.com/SocketDotTech/socket-v2-sdk/blob/72e8f92/src/client/core/CancelablePromise.ts#L98)

---

### then

▸ **then**<`TResult1`, `TResult2`\>(`onFulfilled?`, `onRejected?`): `Promise`<`TResult1` \| `TResult2`\>

#### Type parameters

| Name       | Type    |
| :--------- | :------ |
| `TResult1` | `T`     |
| `TResult2` | `never` |

#### Parameters

| Name           | Type                                                                    |
| :------------- | :---------------------------------------------------------------------- |
| `onFulfilled?` | `null` \| (`value`: `T`) => `TResult1` \| `PromiseLike`<`TResult1`\>    |
| `onRejected?`  | `null` \| (`reason`: `any`) => `TResult2` \| `PromiseLike`<`TResult2`\> |

#### Returns

`Promise`<`TResult1` \| `TResult2`\>

#### Implementation of

Promise.then

#### Defined in

[src/client/core/CancelablePromise.ts:85](https://github.com/SocketDotTech/socket-v2-sdk/blob/72e8f92/src/client/core/CancelablePromise.ts#L85)

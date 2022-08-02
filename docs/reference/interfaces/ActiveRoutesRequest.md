# ActiveRoutesRequest

## Table of contents

### Properties

- [fromChainId](ActiveRoutesRequest.md#fromchainid)
- [fromTokenAddress](ActiveRoutesRequest.md#fromtokenaddress)
- [limit](ActiveRoutesRequest.md#limit)
- [offset](ActiveRoutesRequest.md#offset)
- [routeStatus](ActiveRoutesRequest.md#routestatus)
- [sort](ActiveRoutesRequest.md#sort)
- [toChainId](ActiveRoutesRequest.md#tochainid)
- [toTokenAddress](ActiveRoutesRequest.md#totokenaddress)
- [userAddress](ActiveRoutesRequest.md#useraddress)

## Properties

### fromChainId

• `Optional` **fromChainId**: `string`

Id of sending chain

#### Defined in

[socket-v2-sdk/src/client/models/ActiveRoutesRequest.ts:13](https://github.com/rugamoto/socket-v2-sdk/blob/91d9fe3/src/client/models/ActiveRoutesRequest.ts#L13)

---

### fromTokenAddress

• `Optional` **fromTokenAddress**: `string`

Address of token on source chain.

#### Defined in

[socket-v2-sdk/src/client/models/ActiveRoutesRequest.ts:17](https://github.com/rugamoto/socket-v2-sdk/blob/91d9fe3/src/client/models/ActiveRoutesRequest.ts#L17)

---

### limit

• `Optional` **limit**: `string`

Number of active routes to return in one API call.

#### Defined in

[socket-v2-sdk/src/client/models/ActiveRoutesRequest.ts:9](https://github.com/rugamoto/socket-v2-sdk/blob/91d9fe3/src/client/models/ActiveRoutesRequest.ts#L9)

---

### offset

• `Optional` **offset**: `string`

Offset for fetching active routes.

#### Defined in

[socket-v2-sdk/src/client/models/ActiveRoutesRequest.ts:7](https://github.com/rugamoto/socket-v2-sdk/blob/91d9fe3/src/client/models/ActiveRoutesRequest.ts#L7)

---

### routeStatus

• `Optional` **routeStatus**: `"PENDING"` \| `"COMPLETED"`

Status of the route. The route will only be marked completed if all the user txs have been completed.

#### Defined in

[socket-v2-sdk/src/client/models/ActiveRoutesRequest.ts:11](https://github.com/rugamoto/socket-v2-sdk/blob/91d9fe3/src/client/models/ActiveRoutesRequest.ts#L11)

---

### sort

• `Optional` **sort**: `"updatedAt"` \| `"createdAt"`

Sort param for routes.

#### Defined in

[socket-v2-sdk/src/client/models/ActiveRoutesRequest.ts:5](https://github.com/rugamoto/socket-v2-sdk/blob/91d9fe3/src/client/models/ActiveRoutesRequest.ts#L5)

---

### toChainId

• `Optional` **toChainId**: `string`

Id of destination chain.

#### Defined in

[socket-v2-sdk/src/client/models/ActiveRoutesRequest.ts:15](https://github.com/rugamoto/socket-v2-sdk/blob/91d9fe3/src/client/models/ActiveRoutesRequest.ts#L15)

---

### toTokenAddress

• `Optional` **toTokenAddress**: `string`

Token address on destination chain.

#### Defined in

[socket-v2-sdk/src/client/models/ActiveRoutesRequest.ts:19](https://github.com/rugamoto/socket-v2-sdk/blob/91d9fe3/src/client/models/ActiveRoutesRequest.ts#L19)

---

### userAddress

• **userAddress**: `string`

Address of user starting the route.

#### Defined in

[socket-v2-sdk/src/client/models/ActiveRoutesRequest.ts:3](https://github.com/rugamoto/socket-v2-sdk/blob/91d9fe3/src/client/models/ActiveRoutesRequest.ts#L3)

---
sidebar_position: 1
---

# Quick Start

The Socket SDK allows developers to quickly and easily integrate socket features into their javascript applications.

## Installation

First install the sdk from npm.

Npm:

```
npm i @socket.tech/v2-sdk
```

Yarn:

```
yarn add @socket.tech/v2-sdk
```

## Usage

Import the socket class and create an instance

```ts
import { Socket } from "@socket.tech/v2-sdk";

const socket = new Socket({
  apiKey: "<API_KEY_HERE",
});
```

You are now ready to retrieve data and execute routes.

# @wexond/rpc

Type-safe communication between processes.
No more remembering channel names, parameters order and their types.

> NOTE: Although this package was made mainly for TypeScript, it can be used in JavaScript as well, but it makes no sense then.

[![Discord](https://discordapp.com/api/guilds/307605794680209409/widget.png?style=shield)](https://discord.gg/P7Vn4VX)

## Motivation

Lets say you want to use `Worker` from Node.js `worker_threads` module. To communicate with worker you need to use `worker.postMessage`, which doesn't provide any callback function. You need to listen for messages on worker itself by `worker.on('message')`. If you want to create an async function, which will use worker under the hood, you need to write a lot of code, just to handle the communication. Also there is the type checking problem, which grows with codebase.

This problem occurs in many places like Electron IPC.

If we don't support your platform, you can create communication handler using our core components.

## Installation

```bash
$ npm install @wexond/rpc-core
```

| Platform | Package                | Details                                                                                                                                                                                                                                                                  | Documentation |
| -------- | ---------------------- | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ | ------------- |
| Electron | `@wexond/rpc-electron` | [![NPM](https://img.shields.io/npm/v/@wexond/rpc-electron.svg?style=flat-square)](https://www.npmjs.com/package/@wexond/rpc-electron) [![NPM](https://img.shields.io/npm/dm/@wexond/rpc-electron?style=flat-square)](https://www.npmjs.com/package/@wexond/rpc-electron) | WIP           |
| Node     | `@wexond/rpc-node`     | [![NPM](https://img.shields.io/npm/v/@wexond/rpc-node.svg?style=flat-square)](https://www.npmjs.com/package/@wexond/rpc-node) [![NPM](https://img.shields.io/npm/dm/@wexond/rpc-node?style=flat-square)](https://www.npmjs.com/package/@wexond/rpc-node)                 | WIP           |
| -        | `@wexond/rpc-core`     | [![NPM](https://img.shields.io/npm/v/@wexond/rpc-core.svg?style=flat-square)](https://www.npmjs.com/package/@wexond/rpc-core) [![NPM](https://img.shields.io/npm/dm/@wexond/rpc-core?style=flat-square)](https://www.npmjs.com/package/@wexond/rpc-core)                 | WIP           |  |

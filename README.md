<p align="center">
  <a href="https://drash.land/sockets">
    <img height="200" src="logo.svg" alt="Sockets">
  </a>
  <h1 align="center">Sockets</h1>
</p>
<p align="center">A WebSocket library for <a href="https://github.com/denoland/deno">Deno</a>.</p>
<p align="center">
  <a href="https://github.com/drashland/socketse/releases">
    <img src="https://img.shields.io/github/release/drashland/sockets.svg?color=bright_green&label=latest">
  </a>
  <a href="https://github.com/drashland/sockets/actions">
    <img src="https://img.shields.io/github/workflow/status/drashland/sockets/master?label=ci">
  </a>
  <a href="https://discord.gg/SgejNXq">
    <img src="https://img.shields.io/badge/chat-on%20discord-blue">
  </a>
  <a href="https://twitter.com/drash_land">
    <img src="https://img.shields.io/twitter/url?label=%40drash_land&style=social&url=https%3A%2F%2Ftwitter.com%2Fdrash_land">
  </a>
</p>

---

**_Although Sockets has working code, it is still very much under development and unstable. APIs will change without notice. Sorry for any inconvenience!_**

## Table of Contents
- [Quickstart](#quickstart)
- [Documentation](#documentation)
- [Features](#features)
- [Contributing](#contributing)
- [License](#license)

## Quickstart

Create your server.

```typescript
// File: app.ts

import { Server } from "https://deno.land/x/sockets@v0.5.0/mod.ts";

// Create the server
const server = new Server();

// Run the server
server.run({
  hostname: "127.0.0.1",
  port: 1777,
});

console.log(
  `Server started on ws://${server.hostname}:${server.port}`,
);
```

Run your server.

```
$ deno run --allow-net app.ts
Server started on ws://127.0.0.1:1777
```

Connect to your server using `wscat` and send a `ping` packet.

```
$ npm install -g wscat
$ wscat -c ws://127.0.0.1:1777
> ping
< pong
```

## Documentation

- [Full Documentation](https://drash.land/sockets)

## Features

- JSON encoding
- Zero dependencies

## Contributing

Contributors are welcomed!

Please read through our [contributing guidelines](./.github/CONTRIBUTING.md). Included are directions for opening issues, coding standards, and notes on development.

## License

By contributing your code, you agree to license your contribution under the [MIT License](./LICENSE).

<div align="center">
  <br />
  <p>
    <a href="https://github.com/BurnhamR/discord.js-legacy"><img src="https://cdn.gamercraftstudios.net/uploads/24125/262265/discord.js-legacy-logo.svg" width="546" alt="discord.js-legacy" /></a>
  </p>
  <br />
  <!--<p>
    <a href="https://www.npmjs.com/package/discord.js/v/12.5.3"><img src="https://cdn.gamercraftstudios.net/uploads/24125/262265/44.svg" alt="NPM version" /></a>
    <a href="https://www.npmjs.com/package/discord.js/v/12.5.3"><img src="https://img.shields.io/npm/dt/discord.js.svg?maxAge=3600" alt="NPM downloads" /></a>
  </p>-->
  <p>
    <a href="https://www.npmjs.com/package/discord.js/v/12.5.3"><img src="https://cdn.gamercraftstudios.net/uploads/24125/262265/status.svg" alt="npm install" width="346" /></a>
  </p>
</div>

## Table of contents

- [About](#about)
- [Installation](#installation)
  - [Audio engines](#audio-engines)
  - [Optional packages](#optional-packages)
- [Example Usage](#example-usage)
- [Links](#links)
  - [Extensions](#extensions)
- [Contributing](#contributing)
- [Help](#help)

## About

discord.js-legacy is an unofficial fork of discord.js and is a powerful [Node.js](https://nodejs.org) module that allows you to easily interact with the
[Discord API](https://discord.com/developers/docs/intro).

- Object-oriented
- Predictable abstractions
- Performant
- 100% coverage of the Discord API

## Installation

**Node.js 12.5.3 or newer is required.**  
Ignore any warnings about unmet peer dependencies, as they're all optional.

Without voice support: `npm i discord.js@12.5.3`  
With voice support ([@discordjs/opus](https://www.npmjs.com/package/@discordjs/opus)): `npm i discord.js@12.5.3 @discordjs/opus`  
With voice support ([opusscript](https://www.npmjs.com/package/opusscript)): `npm i discord.js@12.5.3 opusscript`

### Audio engines

The preferred audio engine is @discordjs/opus, as it performs significantly better than opusscript. When both are available, discord.js will automatically choose @discordjs/opus.
Using opusscript is only recommended for development environments where @discordjs/opus is tough to get working.
For production bots, using @discordjs/opus should be considered a necessity, especially if they're going to be running on multiple servers.

### Optional packages

- [zlib-sync](https://www.npmjs.com/package/zlib-sync) for WebSocket data compression and inflation (`npm install zlib-sync`)
- [erlpack](https://github.com/discord/erlpack) for significantly faster WebSocket data (de)serialisation (`npm install discord/erlpack`)
- One of the following packages can be installed for faster voice packet encryption and decryption:
  - [sodium](https://www.npmjs.com/package/sodium) (`npm install sodium`)
  - [libsodium.js](https://www.npmjs.com/package/libsodium-wrappers) (`npm install libsodium-wrappers`)
- [bufferutil](https://www.npmjs.com/package/bufferutil) for a much faster WebSocket connection (`npm install bufferutil`)
- [utf-8-validate](https://www.npmjs.com/package/utf-8-validate) in combination with `bufferutil` for much faster WebSocket processing (`npm install utf-8-validate`)

## Example usage

```js
const Discord = require('discord.js');
const client = new Discord.Client();

client.on('ready', () => {
  console.log(`Logged in as ${client.user.tag}!`);
});

client.on('message', msg => {
  if (msg.content === 'ping') {
    msg.reply('pong');
  }
});

client.login('token');
```

## Links

- [Website](https://discord.js.org/) ([source](https://github.com/BurnhamR/discord.js-legacy))
- [Documentation](https://discord.js.org/#/docs/main/12.5.3/general/welcome)
- [Guide](https://skyy.cc/discord.js-legacy.html) ([source](https://github.com/BurnhamR/discord.js-legacy-guide)) - WIP
  See also the [Update Guide](https://discordjs.guide/additional-info/changes-in-v12.html), including updated and removed items in the library.
- [Discord API Discord server](https://discord.gg/discord-api)
- [GitHub](https://github.com/BurnhamR/discord.js-legacy)
- [NPM](https://www.npmjs.com/package/discord.js/v/12.5.3)
- [Related libraries](https://discordapi.com/unofficial/libs.html)

### Extensions

- [RPC](https://www.npmjs.com/package/discord-rpc) ([source](https://github.com/discordjs/RPC))

## Contributing

Before creating an [issue](https://github.com/BurnhamR/discord.js-legacy/issues), please ensure that it hasn't already been reported/suggested, and double-check the
[documentation](https://skyy.cc/discord.js-legacy.html).  

## Help

If you don't understand something in the documentation, you are experiencing problems, or you just need a gentle
nudge in the right direction, please don't hesitate to join Discord.js's official [Discord.js Server](https://discord.gg/bRCvFy9).
They currently have a djs-v12-deprecated channel to gains support in.
We are currently in the process of making a full wiki for Discord.js-legacy here: [Github Wiki](https://github.com/BurnhamR/discord.js-legacy-guide) & [Official discord.js-legacy documentation](https://skyy.cc/discord.js-legacy.html) & [Official discord.js documentation for v12.5.3](https://discord.js.org/#/docs/main/12.5.3/general/welcome).

## This Fork

This is NOT an official discord.js project and is not marketed as one, this is an updated legacy version of discord.js(pre-discord.js v13) for developers who are not wanting to recode or update there bot just for an update. As well discord.js v13.0.0+ is much more intensive and can be confusing for a beginner developer, so we are creating and updating this project. 

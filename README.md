  <br />
    <p>
    <a href="https://discord.gg/HMUfMXDQsV"><img src="https://cdn.discordapp.com/attachments/843533109818556417/867483427510681600/68747470733a2f2f63646e2e646973636f72646170702e636f6d2f6174746163686d656e74732f3830343530353333353339.png" alt="dbd.ts" /></a>
  </p>

# dbd.ts
[![Discord Server](https://img.shields.io/discord/773352845738115102?color=5865F2&logo=discord&logoColor=white)](https://discord.gg/HMUfMXDQsV)
[![NPM Version](https://img.shields.io/npm/v/dbd.ts.svg?maxAge=3600)](https://www.npmjs.com/package/dbd.ts)
[![NPM Downloads](https://img.shields.io/npm/dt/dbd.ts.svg?maxAge=3600)](https://www.npmjs.com/package/dbd.ts)

  <br />
    <p>
    <a href="https://discord.gg/HMUfMXDQsV"><img src="https://cdn.discordapp.com/attachments/838976217561563197/869269773589049374/68747470733a2f2f63646e2e646973636f72646170702e636f6d2f6174746163686d656e74732f3830343530353333353339.png" alt="dbd.ts" /></a>
  </p>

## Installation

**Node.JS 16.6.0 or newer is required.**

```sh-session
npm install dbd.ts
```

### Example
```js
const dbd = require("dbd.ts")

const bot = new dbd.Bot({
    intents: ["GUILDS", "GUILD_MESSAGES"], //Discord Intents
    prefix: "PREFIX" //Discord Client Prefix
})


bot.addEvent([
    "onMessage"
])

bot.commands.add({
    type: "basicCommand",
    name: "ping",
    code: "Pong! $pingms"
})

bot.login("Discord Bot Token")
```

## Support
If you need support or have questions to ask, you can join our [Discord Server!](https://discord.gg/HMUfMXDQsV)

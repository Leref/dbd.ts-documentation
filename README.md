# ✨ dbd.ts
[![Discord Server](https://img.shields.io/discord/773352845738115102?color=5865F2&logo=discord&logoColor=white)](https://discord.gg/HMUfMXDQsV)
[![NPM Version](https://img.shields.io/npm/v/dbd.ts.svg?maxAge=3600)](https://www.npmjs.com/package/dbd.ts)
[![NPM Downloads](https://img.shields.io/npm/dt/dbd.ts.svg?maxAge=3600)](https://www.npmjs.com/package/dbd.ts)\
DBD.TS is a simple feature-rich package for creating Discord bots.
  <br />
    <p>
    <a href="https://discord.gg/HMUfMXDQsV"><img src="https://cdn.discordapp.com/attachments/838976217561563197/869269773589049374/68747470733a2f2f63646e2e646973636f72646170702e636f6d2f6174746163686d656e74732f3830343530353333353339.png" alt="dbd.ts" /></a>
  </p>

### ⚙️ Installation

**Node.JS 16.6.0 or newer is required.**

```sh-session
npm install dbd.ts
```

### 🛠️ Main File
Once DBD.TS has been installed, you can paste-in and modify this example in your `index.js` file.

```javascript
const dbd = require("dbd.ts")

const bot = new dbd.Bot({
    intents: ["GUILDS", "GUILD_MESSAGES"],
    prefix: "PREFIX"
})

bot.addEvent([
    "onMessage",
    "onInteraction"
])

bot.commands.add({
    type: "basicCommand",
    name: "ping",
    code: `🏓 Pong! $pingms`
})

bot.commands.add({
    type: "basicCommand",
    name: "eval",
    code: `$onlyForIDs[$botOwnerID;]
$eval[$message]`
})

bot.login("TOKEN")
```
> 'PREFIX' must be replaced with a prefix. 'TOKEN' must be replaced with your bot's token. 

### 🔧 Support
If you need support or have questions, you can join our [Discord Server](https://discord.gg/HMUfMXDQsV). We are happy to help!

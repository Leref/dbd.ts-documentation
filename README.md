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

## Plugins Support

To create a plugin, you first need to have a plugins folder in your project environment *(this is not yet customizable)*. <br>
Create a file in that folder with any name you want, and paste this into your code:
```js
/**
 * This below will only work if you are using a proper IDE, so intellisense does it's job.
 * @type {import("dbd.ts").FunctionData}
 */ 
const func = {
    // This would be the name for the plugin or function.
    name: "$systemChannelID",
    
    // You cannot skip this on typescript, but in javascript.
    description: "return system channel id of the guild.",

    // This function is called every time this function is used.
    execute: (d, fn) => {
        // Watch out! data.message will not always be a Message object, so is recommend to use instanceof to check what it actually is before ever returning anything.
        return fn.resolve(
            d.data.message.guild?.systemChannelID
        )
    }
}

// Export function.
module.exports = func

// Belong line would work too
// module.exports.default = func
```
Plugins only support js / ts for now. <br>
This should only be used by user(s) who already know typescript or javascript. <br>
We won't give any support regarding plugins as they are not coded by us and therefore is not of our concern of what happens.

## Other Support 

Slash, Button, Select Menu commands and much more are supported in dbd.ts <br>
It's simple and easy to setup with a few lines of code.</br>

## Support
If you need support or have questions to ask, you can join our [Discord Server!](https://discord.gg/HMUfMXDQsV)

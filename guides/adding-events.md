# Adding Events
```js
bot.addEvent([
    "onMessage", //every bot should have this
    "event2",
    "event3"
])
```

### Example
> This example adds every event currently available to the bot. This is not recommended, as you shouldn't use events you don't need. Feel free to edit this code to your needs.
```js
const dbd = require("dbd.ts")

const bot = new dbd.Bot({
    intents: ["GUILDS", "GUILD_MESSAGES"],
    prefix: "PREFIX"
})

bot.addEvent([
    "onMessage",
    "onReady",
    "onInteraction",
    "onJoin",
    "onLeave",
    "onBotJoin",
    "onBotLeave",
    "onReactionAdd",
    "onReactionRemove",
    "onLavalinkSongStart",
    "onLavalinkSongFinish"
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

### Events
- onMessage
- onReady
- onInteraction
- onJoin
- onLeave
- onBotJoin
- onBotLeave
- onReactionAdd
- onReactionRemove
- onLavalinkSongStart
- onLavalinkSongFinish

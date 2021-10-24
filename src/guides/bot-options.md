# Bot Options
Customize your bot and experience with DBD.TS using bot options! ✨

### Example With Additional Options
```js
const dbd = require("dbd.ts")

const bot = new dbd.Bot({
    intents: ["GUILDS", "GUILD_MESSAGES"],
    prefix: "!",
    ignoreAllErrors: true,
    insensitive: true,
    reverseReading: true,
    internalSharding: false
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

### Options
#### ignoreAllErrors
*(false by default)*
```yml
ignoreAllErrors: boolean
```
Suppresses all errors thrown by the interpreter and outputs nothing instead, this can be overriden in commands.

#### insensitive
*(false by default)*
```yml
insensitive: boolean
```
Whether the functions can be read as case insensitive.


#### intents
```yml
intents: ["intent1", "intent2", "intent3"]
```
The [intents](https://discord.js.org/#/docs/main/stable/class/Intents?scrollTo=s-FLAGS) for this bot.

#### internalSharding
*(false by default)*
```yml
internalSharding: boolean
```
Whether to use internal sharding on this bot.

#### prefix
```yml
prefix: ["prefix1", "prefix2", "prefix3"]
```
OR
```yml
prefix: "string"
```
The prefix or prefixes for this bot.

#### reverseReading
*(false by default)*
```yml
reverseReading: boolean
```
Reverses code reading of functions *(bottom to top, right to left. Instead of top to bottom, left to right)*, this can be changed in commands.

#### token
```yml
token: string
```
The token for this bot.

---
description: Command executes when a user joins the guild. 
---
# onJoin

### Prerequisites 
**Adding the onJoin Event:**
{% tabs %} {% tab title="index.js" %}
```js
bot.addEvent([
    "onMessage",
    "onJoin" //This is what you need to add
])
```

**Add the `GUILD_MEMBERS` Intent:**
```js
const dbd = require("dbd.ts")

const bot = new dbd.Bot({
    intents: ["GUILDS", "GUILD_MESSAGES", "GUILD_MEMBERS"],
    prefix: "PREFIX"
})
//Add the rest of your index.js here
```

**Enable Prilivaged "Members Intent" in the [Discord Developer Portal](https://discord.com/developers/applications):**\
![](https://user-images.githubusercontent.com/69215413/132259963-80061d84-6243-46d3-9d04-7e3d729fcc48.png)

### Example
```js
bot.commands.add({
  type: "joinCommand",
  code: `$channelSendMessage[773363417338609674;Welcome <@$authorID>!]`
})
```

![Result](https://user-images.githubusercontent.com/69215413/132259727-9352ba7b-ca2b-4e0c-baec-259e7dae9ff6.png)

{% hint style="warning" %}
You should use server variables in `$channelSendMessage[]` *(if your bot is in more than 1 server)*.
{% endhint %}

---
description: Command executes when a user leaves the guild. 
---
# onLeave
**Event:** `onLeave`\
**Type:** `leaveCommand`

### Prerequisites 
**Add the `onLeave` Event:**
{% tabs %} {% tab title="index.js" %}
```javascript
bot.addEvent([
    "onMessage",
    "onInteraction",
    "onLeave" //This is what you need to add
])
```
{% endtab %} {% endtabs %}


**Add the `GUILD_MEMBERS` Intent:**
{% tabs %} {% tab title="index.js" %}
```javascript
const dbd = require("dbd.ts")

const bot = new dbd.Bot({
    intents: ["GUILDS", "GUILD_MESSAGES", "GUILD_MEMBERS"],
    prefix: "PREFIX"
})
//The rest of your index.js file here
```
{% endtab %} {% endtabs %}

**Enable Prilivaged "Members Intent" in the [Discord Developer Portal](https://discord.com/developers/applications):**\
![](https://user-images.githubusercontent.com/69215413/132259963-80061d84-6243-46d3-9d04-7e3d729fcc48.png)

### Example
```javascript
bot.commands.add({
  type: "leaveCommand",
  code: `$channelSendMessage[773363417338609674;Sad to see $userTag[$authorID] go :(]`
})
```
![Result](https://user-images.githubusercontent.com/69215413/138601897-9e9701b4-c893-4945-af37-cb29cef94754.png)

{% hint style="warning" %}
You should use server variables in `$channelSendMessage[]` *(if your bot is in more than 1 server)*.
{% endhint %}
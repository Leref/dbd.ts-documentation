---
description: Command executes when a reaction gets added to a message.
---
# onReactionAdd
**Event:** `onReactionAdd`\
**Type:** `reactionAddCommand`

### Prerequisites 
**Add the `onReactionAdd` Event:**
{% tabs %} {% tab title="index.js" %}
```javascript
bot.addEvent([
    "onMessage",
    "onInteraction",
    "onReactionAdd" //This is what you need to add
])
```
{% endtab %} {% endtabs %}

**Add the `GUILD_MESSAGE_REACTIONS` Intent:**
{% tabs %} {% tab title="index.js" %}
```javascript
const dbd = require("dbd.ts")

const bot = new dbd.Bot({
    intents: ["GUILDS", "GUILD_MESSAGES", "GUILD_MESSAGE_REACTIONS"], //You add the intent to this array, as shown
    prefix: "PREFIX"
})
//The rest of your index.js file here
```
{% endtab %} {% endtabs %}

### Functions
* `$emojiString` - The stringified emoji an user reacted with.
* `$emojiID` - The ID of the emoji an user reacted with.
* `$emojiName` - The name of the emoji an user reacted with.
* `$emojiIdentifier` - The identifier of the emoji an user reacted with.
* `$reactionAuthorID` - Returns the user who reacted.

### Example
```javascript
bot.commands.add({
  type: "reactionAddCommand",
  code: `$channelSendMessage[773363417338609674;
**New Reaction**
Emoji ID: $emojiID
Identifier: $emojiIdentifier
Name: $emojiName
String: $emojiString
Author: $userTag[$reactionAuthorID] ($reactionAuthorID)]`
})
```
![Result](https://user-images.githubusercontent.com/69215413/138615340-80c8bb3f-7aaf-413c-a670-5a5c832e1ad9.png)

{% hint style="warning" %}
You should use server variables in `$channelSendMessage[]` for 'channelID' *(if your bot is in more than 1 server)*.
{% endhint %}
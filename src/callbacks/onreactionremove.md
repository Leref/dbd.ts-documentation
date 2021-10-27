---
description: Command executes when a reaction gets removed from a message.
---
# onReactionRemove
**Event:** `onReactionRemove`\
**Type:** `reactionRemoveCommand`

### Prerequisites 
**Add the `onReactionRemove` Event:**
{% tabs %} {% tab title="index.js" %}
```javascript
bot.addEvent([
    "onMessage",
    "onInteraction",
    "onReactionRemove" //This is what you need to add
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
* `$emojiString` - The stringified emoji an user unreacted with.
* `$emojiID` - The ID of the emoji an user unreacted with.
* `$emojiName` - The name of the emoji an user unreacted with.
* `$emojiIdentifier` - The identifier of the emoji an user unreacted with.
* `$reactionAuthorID` - Returns the user who unreacted.

### Example
```javascript
bot.commands.add({
  type: "reactionRemoveCommand",
  code: `$channelSendMessage[773363417338609674;
**Removed Reaction**
Emoji ID: $emojiID
Identifier: $emojiIdentifier
Name: $emojiName
String: $emojiString
Author: $userTag[$reactionAuthorID] ($reactionAuthorID)]`
})
```
![Result](https://user-images.githubusercontent.com/69215413/138615507-05589a1d-da92-490a-af6e-0088d77d6b1f.png)

{% hint style="warning" %}
You should use server variables in `$channelSendMessage[]` for 'channelID' *(if your bot is in more than 1 server)*.
{% endhint %}
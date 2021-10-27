---
description: Command executes when the bot gets added to a new guild. 
---
# onBotJoin
**Event:** `onBotJoin`\
**Type:** `botJoinCommand`

### Prerequisites 
**Add the `onBotJoin` Event:**
{% tabs %} {% tab title="index.js" %}
```javascript
bot.addEvent([
    "onMessage",
    "onInteraction",
    "onBotJoin" //This is what you need to add
])
```
{% endtab %} {% endtabs %}

### Example
```javascript
bot.commands.add({
  type: "botJoinCommand",
  code: `$channelSendMessage[773363417338609674;
 $title[1;New Guild]
 $color[1;RANDOM]
 $description[1;Guild Name: $serverName[$guildID]
 Guild ID: $guildID]]`
})
```
![Result](https://user-images.githubusercontent.com/69215413/138603207-bcbba678-226d-4761-bc65-28f98992c302.png)
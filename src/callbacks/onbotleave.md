---
description: Command executes when the bot gets removed/kicked from a guild. 
---
# onBotLeave
**Event:** `onBotLeave`\
**Type:** `botLeaveCommand`

### Prerequisites 
**Add the `onBotLeave` Event:**
{% tabs %} {% tab title="index.js" %}
```javascript
bot.addEvent([
    "onMessage",
    "onInteraction",
    "onBotLeave" //This is what you need to add
])
```
{% endtab %} {% endtabs %}

### Example
```javascript
bot.commands.add({
  type: "botLeaveCommand",
  code: `$channelSendMessage[773363417338609674;
 $title[1;Removed from Guild]
 $color[1;RED]
 $description[1;Guild Name: $serverName[$guildID]
 Guild ID: $guildID]]`
})
```
![Result](https://user-images.githubusercontent.com/69215413/138603507-800dd48d-b008-47ca-a4a6-046bf71375e8.png)
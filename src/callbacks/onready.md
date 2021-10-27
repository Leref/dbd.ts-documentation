---
description: Command executes when the bot gets added to a new guild. 
---
# onReady
**Event:** `onReady`\
**Type:** `readyCommand`

### Prerequisites 
**Adding the `onReady` Event:**
{% tabs %} {% tab title="index.js" %}
```javascript
bot.addEvent([
    "onMessage",
    "onInteraction",
    "onReady" //This is what you need to add
])
```
{% endtab %} {% endtabs %}

### Example
```javascript
bot.commands.add({
  type: "readyCommand",
  code: `$channelSendMessage[773363417338609674;I'm ready! :rocket:]`
})
```
![Result](https://user-images.githubusercontent.com/69215413/138604215-effc6e73-90b7-4d42-aaa0-e1cf841b24e8.png)
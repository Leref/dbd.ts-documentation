---
description: Makes this interaction response ephemeral.
---
# $ephemeral
### Usage
```php
$ephemeral
```

[What does ephemeral mean? (click me)](https://support.discord.com/hc/en-us/articles/1500000580222-Ephemeral-Messages-FAQ)

{% hint style="danger" %} Ephemeral messages can only be used for interactions (slash commands, buttons, select menus, context menus, etc) {% endhint %} 
 
### Example
```javascript
bot.commands.add({
  type: "slashCommand",
  name: "example",
  code: `$ephemeral
Hello World!`
})
```
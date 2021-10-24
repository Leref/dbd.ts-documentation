---
description: Fetches members of a guild.
---
# $fetchGuildMembers
### Usage
```php
$fetchGuildMembers[guildID]
```

{% hint style="info" %} `$fetchGuildMembers` doesn't return any output. {% endhint %}

### Example
```javascript
bot.commands.add({
    type: "basicCommand",
    name: "example",
    code: `$fetchGuildMembers[$guildID]` //Fetches the current guild's members
})
```

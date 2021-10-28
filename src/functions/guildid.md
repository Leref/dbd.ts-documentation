---
description: Returns the guild's ID.
---

# $guildID
### Usage
```php
$guildID
```
### Example
```javascript
bot.commands.add({
  type: "basicCommand",
  name: "example",
  code: `This guild ID is $guildID`
})
```
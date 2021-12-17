---
description: Returns the ping of the bot's database.
---

# $dbPing
### Usage
```php
$dbPing
```

### Example
```javascript
bot.commands.add({
  type: "basicCommand",
  name: "example",
  code: `Database Ping: \`$dbPingms\``
})
```
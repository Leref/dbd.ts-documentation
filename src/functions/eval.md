---
description: Evals the provided DBD.TS code.
---
# $eval
### Usage
```php
$eval[code]
```

### Examples
```javascript
bot.commands.add({
  type: "basicCommand",
  name: "example",
  code: `$onlyForIDs[$botOwnerID;]
$eval[$message]` //Evals the provided code
})
```
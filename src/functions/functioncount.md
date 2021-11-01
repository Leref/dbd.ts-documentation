---
description: Returns how many functions there currently are in DBD.TS.

# $functionCount
### Usage
```php
$functionCount
```

### Example
```javascript
bot.commands.add({
    type: "basicCommand",
    name: "example",
    code: `There \`$functionCount\` functions in DBD.TS!`
})
```
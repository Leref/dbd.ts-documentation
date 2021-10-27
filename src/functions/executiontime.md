---
description: Returns the execution time between container creation and current functions that were executed.
---
# $executionTime
### Usage
```php
$executionTime
```

### Example
```javascript
bot.commands.add({
    type: "basicCommand",
    name: "example",
    code: `(code here)
    $channelSendMessage[$channelID;$executionTime]` //Returns the execution time of the code in a new message
})
```
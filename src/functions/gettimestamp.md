---
description: Gets current timestamp since 1970.
---

# $getTimestamp
### Usage
```php
$getTimestamp
```

### Example
```js
bot.commands.add({
  type: "basicCommand",
  name: "timestamp",
  code: `Current Timestamp is $getTimestamp` //Example: Returns: "Current Timestamp is 1635384460315"
})
```

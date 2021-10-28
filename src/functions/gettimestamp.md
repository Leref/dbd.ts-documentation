---
description: Gets current timestamp since 1970 in milliseconds.
---

# $getTimestamp
### Usage
```php
$getTimestamp
```

### Example
```javascript
bot.commands.add({
  type: "basicCommand",
  name: "example",
  code: `Current Timestamp is $getTimestamp` //Returns "Current Timestamp is 1635384460315"
})
```
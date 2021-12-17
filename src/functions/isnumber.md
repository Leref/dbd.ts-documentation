---
description: Checks whether given value is a number.
---

# $isNumber
### Usage
```php
$isNumber[value]
```

This function has one param.

| Param | Description | Type | Required |
| :--- | :--- | :--- | :--- |
| value | The value to check. | String | Yes |

### Examples
**Example #1**
```javascript
bot.commands.add({
    type: "basicCommand",
    name: "example",
    code: `$isNumber[1]` //Returns true
})
```

**Example #2**
```javascript
bot.commands.add({
    type: "basicCommand",
    name: "example",
    code: `$isNumber[e]` //Returns false
})
```
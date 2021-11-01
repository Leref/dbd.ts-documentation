---
description: Checks whether given value is a number.
---

# $isNumber
### Usage
```php
$isNumber[value]
```

This function has one field.

| Field | Description | Type | Required |
| :--- | :--- | :--- | :--- |
| value | The value to check. | string | yes |

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
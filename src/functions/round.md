---
description: Rounds a floating-point number to the nearest unit.
---

# $round
### Usage
```php
$round[number;unit]
```

This function has two fields.

| Field | Description | Type | Required |
| :--- | :--- | :--- | :--- |
| number | The number to round. | number | yes
| unit | Amount of decimals to leave. | integer | yes

### Examples
**Example #1**
```javascript
bot.commands.add({
    type: "basicCommand",
    name: "example",
    code: `$round[10.5836763;0]` //Returns 11
})
```
**Example #2**
```javascript
bot.commands.add({
    type: "basicCommand",
    name: "example",
    code: `$round[10.5836763;1]` //Returns 10.6
})
```
**Example #3**
```javascript
bot.commands.add({
    type: "basicCommand",
    name: "example",
    code: `$round[1000.389;2]` //Returns 1000.39
})
```
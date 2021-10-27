---
description: Divides the provided numbers.
---
# $divide
### Usage
```php
$divide[numbers]
```

This function has one field.

| Field | Description | Type | Required |
| :--- | :--- | :--- | :--- |
| numbers | The numbers to divide, separated by `;`. | number | yes

### Examples
**Example #1**
```javascript
bot.commands.add({
    type: "basicCommand",
    name: "example",
    code: `$divide[10;5]` //Returns 2
})
```
**Example #2**
```javascript
bot.commands.add({
    type: "basicCommand",
    name: "example",
    code: `$divide[25;5]` //Returns 5
})
```
**Example #3**
```javascript
bot.commands.add({
    type: "basicCommand",
    name: "example",
    code: `$divide[150;10]` //Returns 15
})
```
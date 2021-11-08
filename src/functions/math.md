---
description: Calculates a math expression.
---

# $math
### Usage
```php
$math[expression]
```

This function has one field.

| Field | Description | Type | Required |
| :--- | :--- | :--- | :--- |
| expression |  The math expression to solve. | string | yes |

**Math Symbols:**
- `+` - Addition.
- `-` - Subtraction.
- `/` - Division.
- `*` - Multiplication.
- `()` - Parentheses you can put equations in.

### Examples
**Addition**
```javascript
bot.commands.add({
    type: "example",
    name: "example",
    code: `$math[1+1]` //Returns 1
})
```
**Subtraction**
```javascript
bot.commands.add({
    type: "basicCommand",
    name: "example",
    code: `$math[10-5]` //Returns 5
})
```
**Multiplication**
```javascript
bot.commands.add({
    type: "basicCommand",
    name: "example",
    code: `$math[2*2]` //Returns 4
})
```
**Division**
```javascript
bot.commands.add({
    type: "basicCommand",
    name: "example",
    code: `$math[32/4]` //Returns 8
})
```
**Mixing Operations**
```javascript
bot.commands.add({
    type: "basicCommand",
    name: "example",
    code: `$math[5-((30/2)*2)+10]` //Returns -15
})
```

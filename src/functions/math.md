---
Description: This function takes in a math expression and returns the answer.
---

# $math
### Usage
```php
$math[operation]
```

This function has one field.

| Field | Description | Type | Required |
| :--- | :--- | :--- | :--- |
| operation | Calculate something | number | yes |

### Example: Addition
```javascript
bot.commands.add({
    type: "basicCommand",
    name: "exampleAddition",
    code: `$math[1+1]`
})
```
```javascript
//returns 2
```

### Example: Subtraction
```javascript
bot.commands.add({
    type: "basicCommand",
    name: "exampleSubtraction",
    code: `$math[10-5]`
})
```
```javascript
//returns 5
```

### Example: Multiplication
```javascript
bot.commands.add({
    type: "basicCommand",
    name: "exampleMultiplication",
    code: `$math[2*2]`
})
```
```javascript
//returns 4
```

### Example: Division
```javascript
bot.commands.add({
    type: "basicCommand",
    name: "exampleDivision",
    code: `$math[32/4]`
})
```
```javascript
//returns 8
```

```javascript
// Symbols:
+ (Addition)
- (Subtraction)
/ (Division)
* (Multiplication)
```

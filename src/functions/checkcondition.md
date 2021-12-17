---
description: Checks if the given condition is true or false.
---

# $checkCondition
### Usage
```php
$checkCondition[value1(comparisonSymbol)value2]
```
This function has three params.

| Param | Description | Type | Required |
| :--- | :--- | :--- | :--- |
| value1 | The value to compare to value 2. | String | Yes |
| (comparisonSymbol) | The comparison symbol | String [(ComparisonSymbol)](typedefs/comparisonsymbols.md) | Yes
| value2 | The value to compare to value 1. | String | Yes |

### Example
```js
bot.commands.add({
  type: "basicCommand",
  name: "condition",
  code: `Given condition: 1>2
  The given condition is $checkCondition[1>2]`
})
```
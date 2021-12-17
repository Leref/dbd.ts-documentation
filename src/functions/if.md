---
description: Creates a condition and executes a code depending on the condition.
---
# $if

### Usage
```php
$if[condition;if true;if false]
```

This function has three params.

| Param | Description | Type | Required |
| :--- | :--- | :--- | :--- |
| condition | The condition to test, uses [ComparisonSymbols](/src/typedefs/comparisonsymbols.md). | String | Yes |
| if true | The code to execute if the condition is true. | String | Yes
| if false | The code to execute if the condition is false. | String | No

### Examples
#### Example #1
```javascript
bot.commands.add({
    type: "basicCommand",
    name: "example",
    code: `
$if[$isNumber[$message]==true;
Message is a number!
;
Message is not a number!]
`
})
```

#### Example #2
*This example showcases how you can use `$if` statement layering. `$if` statement layering is using `$if` statements within other `$if` statements.*
```javascript
bot.commands.add({
    type: "basicCommand",
    name: "example",
    code: `
  $if[$packageVersion==3.0.0;
    v3 😔
;
  $if[$packageVersion==4.0.0;
    Hallelujah v4
;
    v$packageVersion
  ]] 
`
})
```

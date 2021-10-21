---
description: Returns the character index of a 'query' within 'text'.
---
# $indexOf
### Usage
```php
$indexOf[text;query]
```

This function has two fields.

| Field | Description | Type | Required |
| :--- | :--- | :--- | :--- |
| text | The text that gets searched for 'query'. | string | yes |
| query | The phrase/character to find within 'text'. | string | yes |

{% hint style="danger" %} Remember the case of characters in `$indexOf[]` matters (e.g. searching for a lowercase `h` within `Hello` won't work). You can use [`$toLowerCase[]`](functions/tolowercase.md) to negate this issue. {% endhint %}

### Examples
#### Example #1
```javascript
bot.commands.add({
    type: "basicCommand",
    name: "example",
    code: `$indexOf[hi hello hey;hey]` //Returns 10
})
```

#### Example #2
```javascript
bot.commands.add({
    type: "basicCommand",
    name: "example",
    code: `$indexOf[DBD.TS is cool.;is]` //Returns 8
})
```

#### Example #3
```javascript
bot.commands.add({
    type: "basicCommand",
    name: "example",
    code: `$indexOf[DBD.TS is cool.;DBD.TS]` //Returns 1
})
```

#### Example #4
```javascript
bot.commands.add({
    type: "basicCommand",
    name: "example",
    code: `$indexOf[This is a example text!;t]` //Returns 19
})
```

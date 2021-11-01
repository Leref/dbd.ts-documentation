---
description: Returns how many arguments are in the user's message, or the provided text.
---
# $argCount
### Usage
```php
$argCount or $argCount[text]
```

This function has one field.

| Field | Description | Type | Required
| :--- | :--- | :--- | :---
| text | The text to get the argument count of. | string | no

{% hint style="info" %} `$argCount` (without brackets) returns how many argument(s) are in the user's message, while `$argCount[text]` returns how many argument(s) are in the provided 'text'. Remember, argument(s) is another meaning for a word; so one word is one argument. {% endhint %}

### Examples
**Example #1**
```javascript
bot.commands.add({
    type: "basicCommand",
    name: "example",
    code: `$argCount` //Returns the argument count of the user's message
})
```
**Example #2**
```javascript
bot.commands.add({
    type: "basicCommand",
    name: "example",
    code: `$argCount[DBD.TS is cool.]` //Returns 3
})
```
**Example #3**
```javascript
bot.commands.add({
    type: "basicCommand",
    name: "example",
    code: `$argCount[Hello World]` //Returns 2
})
```
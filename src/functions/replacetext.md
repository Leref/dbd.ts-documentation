---
description: Replaces something with something else in the provided text.
---

# $replaceText
### Usage
```php
$replaceText[text;sample;new;howMany]
```

This function has four fields.

| Field | Description | Type | Required |
| :--- | :--- | :--- | :--- |
| text | The text that gets searched for 'sample'. | String | Yes
| sample | The text to replace with 'new'. | String | Yes
| new | The text to replace 'sample' with. | String | Yes
| howMany | How many samples shall be replaced with 'new', all by default. | Integer | No

### Examples
**Example #1**
```javascript
bot.commands.add({
    type: "basicCommand",
    name: "example",
    code: `$replaceText[Hello World!;World;Planet]` //Returns "Hello Planet!"
})
```
**Example #2**
```javascript
bot.commands.add({
    type: "basicCommand",
    name: "example",
    code: `$replaceText[DBD.TS is very very epic;very very;extremely]` //Returns "DBD.TS is extremely epic"
})
```
**Example #3**
```javascript
bot.commands.add({
    type: "basicCommand",
    name: "example",
    code: `$replaceText[Leref is Leref;Leref;That person;1]` //Returns "That person is Leref"
})
```
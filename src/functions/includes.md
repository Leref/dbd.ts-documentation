---
description: Checks whether given text contains something.
---
# $includes
### Usage
```php
$includes[text;queries]
```
This function has two fields.

| Field | Description | Type | Required |
| :--- | :--- | :--- | :--- |
| text | The text to search for 'queries' | string | yes |
| queries | The arguments that 'text' shall contain, separated by `;`. | string | yes

{% hint style="danger" %} Remember the case of characters in `$includes[]` matters (e.g. searching for a lowercase `h` within `Hello` would return 'false', not 'true'.). You can use [`$toLowerCase[]`](./tolowercase.md) to negate this issue. {% endhint %}

### Examples
#### Example #1
```javascript
bot.commands.add({
    type: "basicCommand",
    name: "example",
    code: `$includes[Hello World!;Hello]` //Returns true
})
```
#### Example #2
```javascript
bot.commands.add({
    type: "basicCommand",
    name: "example",
    code: `$includes[DBD.TS is cool!;cool;easy]
$includes[DBD.TS is cool and easy!;cool;easy]
$includes[DBD.TS is easy!;cool;easy]` //All 3 statements would return true
})
```
#### Example #3
```javascript
bot.commands.add({
    type: "basicCommand",
    name: "example",
    code: `$includes[Hello Planet;Earth]` //Returns false
})
```

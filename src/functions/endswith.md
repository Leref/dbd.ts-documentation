---
description: Returns whether the provided text's last argument is 'query'.
---

# $endsWith
### Usage
```php
$endsWith[text;query]
```

This function has two fields.

| Field | Description | Type | Required 
| :---- | :---- | :---- | :----
| text | The text that may end with 'query'. | string | yes
| query | The word that 'text' may end with. | string | yes

{% hint style="danger" %} Remember the case of characters in `$endsWith[]` matters (e.g. `$endsWith[HELLO;o]` would return false). You can use [`$toLowerCase[]`](./tolowercase.md) to negate this issue. {% endhint %}

### Examples
**Example #1**
```javascript
bot.commands.add({
    type: "basicCommand",
    name: "example",
    code: `$endsWith[Hello World;World]` //Returns true
})
```

**Example #2**
```javascript
bot.commands.add({
    type: "basicCommand",
    name: "example",
    code: `$endsWith[Hello World;Hello]` //Returns false
})
```
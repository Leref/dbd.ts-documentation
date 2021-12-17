---
description: Removes excess/useless spaces from the provided text.
---

# $makeReturn
### Usage
```php
$makeReturn[text]
```

This function has one param.

| Param | Description | Type | Required |
| :---- | :---- | :---- | :----
| text | The text to remove excess spacing from. | String | Yes

### Example
```javascript
bot.commands.add({
    type: "basicCommand",
    name: "example",
    code: `$makeReturn[a   b   c]` //Returns "a b c"
})
```
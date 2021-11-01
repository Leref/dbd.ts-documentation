---
description: Removes excess/useless spaces from the provided text.
---

# $makeReturn
### Usage
```php
$makeReturn[text]
```

| Field | Description | Type | Required |
| :---- | :---- | :---- | :----
| text | The text to remove excess spacing from. | string | yes

### Example
```javascript
bot.commands.add({
    type: "basicCommand",
    name: "example",
    code: `$makeReturn[a   b   c]` //Returns "a b c"
})
```
---
description: Deletes the author's message.
---

# $deletecommand
### Usage
```php
$deletecommand[duration]
```

This function has one field.

| Fields | Description | Type | Required |
| :--- | :--- | :--- | :--- |
| duration | How long to wait before deleting the author's message. | time | no |

### Example
```javascript
bot.commands.add({
    type: "basicCommand",
    name: "example",
    code: `$deletecommand` //Deletes the author's message instantly
})
```
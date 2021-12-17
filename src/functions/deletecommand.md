---
description: Deletes the author's message.
---

# $deletecommand
### Usage
```php
$deletecommand[duration]
```

This function has one param.

| Param | Description | Type | Required |
| :--- | :--- | :--- | :--- |
| duration | How long to wait before deleting the author's message. **\*** | Time | No |
**\*** Deletes the author's message instance if no `duration` is provided.

### Example
```javascript
bot.commands.add({
    type: "basicCommand",
    name: "example",
    code: `$deletecommand` //Deletes the author's message instantly
})
```
---
description: Logs something to the console.
---
# $log
### Usage
```php
$log[text]
```

This function has one field.

| Field | Description | Type | Required |
| :--- | :--- | :--- | :--- |
| text | The text to log. | string | yes |

### Example
```javascript
bot.commands.add({
    type: "basicCommand",
    name: "example",
    code: `$log[Hello World!]`
})
```

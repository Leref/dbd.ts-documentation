---
description: Logs something to the console.
---
# $log
### Usage
```php
$log[text]
```

This function has one param.

| Param | Description | Type | Required |
| :--- | :--- | :--- | :--- |
| text | The text to log. | String | Yes |

### Example
```javascript
bot.commands.add({
    type: "basicCommand",
    name: "example",
    code: `$log[Hello World!]`
})
```

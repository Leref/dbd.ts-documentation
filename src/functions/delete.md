---
description: Deletes a temporary variable that was set with $let.
---

# $delete
### Usage
```php
$delete[variableName]
```
This function has one param.

| Params | Description | Type | Required |
| :--- | :--- | :--- | :--- |
| variableName | The temporary variable to delete. | String | Yes |

### Example
```javascript
bot.commands.add({
  type: "basicCommand",
  name: "example",
  code: `$let[text;Hello!]
$get[text]
$delete[text]`
})
```
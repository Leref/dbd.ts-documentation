---
description: Deletes a temporary variable that was set with $let.
---

# $delete
### Usage
```php
$delete[variableName]
```
This function has one field.
| Field | Description | Type | Required |
| :--- | :--- | :--- | :--- |
| variableName | The temporary variable to delete. | string | yes |

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
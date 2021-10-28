---
description: Creates a temporary variable.
---

# $let
{% hint style="info" %}
Temporary variables store data that can be used later in the code and are deleted once the code is executed.
{% endhint %}

### Usage
```php
$let[variableName;variableValue]
```
This function has two fields.
| Field | Description | Type | Required |
| :--- | :--- | :--- | :--- |
| variableName | The name of this variable. | string | yes |
| variableValue | The value that this variable holds. | string | yes |

### Example
```javascript
bot.commands.add({
  type: "basicCommand",
  name: "example",
  code: `$let[user;$mentioned[1]]
$description[1;<@$get[user]>]
$addField[1;ID;$get[user]]
$addField[1;Roles;$userRoles[$guildID;$get[user];yes;mention]]
$addField[1;Permissions;$userPerms[$guildID;$get[user];, ;yes]]`
})
```

### Related Functions
- [`$get[]`](functions/get.md) - Gets the currency value of a temporary variable.
- [`$delete[]`](functions/delete/md) - Deletes the provided variable, so it can no longer be used in the code.
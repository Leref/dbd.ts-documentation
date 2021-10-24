---
description: Deletes the provided roles.
---
# $deleteRoles
### Usage
```php
$deleteRoles[guildID;reason;roleIDs]
```
This function has three fields.

| Field | Description | Type | Required |
| :--- | :--- | :--- | :--- |
| guildID | The guild these role(s) belong to. | snowflake | yes |
| reason | The reason for deleting these roles. | string | yes |
| roleIDs | The roles to delete, separated by `;`. | snowflake | yes |

### Example
```js
bot.commands.add({
  type: "basicCommand",
  name: "example",
  code: `$onlyIf[$hasPerm[$guildID;$authorID;manageroles]==true;Missing permissions!]
$deleteRoles[$guildID;;$mentionedRoles[1]]
Deleted role!`
})
```

---
description: Kick an user from a guild.
---
# $kick
### Usage
```php
$kick[guildID;userID;reason]
```

This function has three fields.

| Field | Description | Type | Required |
| :--- | :--- | :--- | :--- |
| guildID | The guild to kick the user from. | Guild | yes |
| userID | The user to kick. | Member | yes |
| reason | The reason for kicking this user. | string | no |

### Example
```javascript
bot.commands.add({
    type: "basicCommand",
    name: "example",
    code: `$kick[773352845738115102;638854865854136320;Kicked]`
})
```

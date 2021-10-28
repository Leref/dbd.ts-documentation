---
description: Bans a user.
---

# $ban
### Usage
```php
$ban[guildID;userID;reason;days]
```

This function has four fields.

| Field | Description | Type | Required |
| :--- | :--- | :--- | :--- |
| guildID | The guild to ban this user from. | snowflake | yes |
| userID | The user to ban from this guild. | snowflake | yes |
| reason | The reason for this ban. | string | no
| deleteDays | Number of days of messages to delete, must be between 0 and 7 inclusive. | integer | no 

### Example
```javascript
bot.commands.add({
    type: "basicCommand",
    name: "ban",
    code: `$ban[$guildID;$mentioned[1;no];$messageSlice[1]]
    $argsCheck[>1;Invalid argument provided! Usage: \`!ban (user) (reason)\`
    $onlyIf[$hasPerm[$guildID;$authorID;ban]==true;You are missing the 'ban' permission.]`
})
```
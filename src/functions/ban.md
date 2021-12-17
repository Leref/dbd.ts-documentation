---
description: Bans a user.
---

# $ban
### Usage
```php
$ban[guildID;userID;reason;days]
```

This function has four params.

| Param | Description | Type | Required |
| :--- | :--- | :--- | :--- |
| guildID | The guild to ban this user from. | Snowflake | Yes |
| userID | The user to ban from this guild. | Snowflake | Yes |
| reason | The reason for this ban. | String | No
| deleteDays | Number of days of messages to delete, must be between 0 and 7 inclusive. | Integer | No 

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
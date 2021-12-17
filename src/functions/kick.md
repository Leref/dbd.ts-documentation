---
description: Kicks a user from the server.
---

# $kick
### Usage
```php
$kick[guildID;userID;reason]
```

This function has three params.

| Param | Description | Type | Required |
| :--- | :--- | :--- | :--- |
| guildID | The server to kick the user from. | Snowflake | Yes |
| userID | The user to kick. | Snowflake | Yes |
| reason | The reason for kicking this user. | String | No |

### Example
```javascript
bot.commands.add({
    type: "basicCommand",
    name: "example",
    code: `$onlyIf[$hasPerm[$guildID;$authorID;kickmembers]==true;You're missing the 'kick' permission!]
$kick[$guildID;$mentioned[1];$noMentionMessage]` //Kicks the mentioned user
})
```
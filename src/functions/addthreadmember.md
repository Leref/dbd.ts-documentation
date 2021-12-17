---
description: Adds a member to the thread.
---

# $addThreadMember
### Usage
```php
$addThreadMember[guildID;threadID;userID;reason]
```

This function has four params.

| Param | Description | Type | Required |
| :--- | :--- | :--- | :--- |
| guildID | The guild that this thread channel belongs to. | Snowflake | Yes |
| threadID | The thread to add this user to. | Snowflake | Yes |
| userID | The user to add to this thread. | Snowflake | Yes |
| reason | The reason for adding this user to the thread. | String | No |

### Example
```javascript
bot.commands.add({
  type: "basicCommand",
  name: "example",
  code: `$guildID[$guildID;123456789123456789;$authorID]`
})
```
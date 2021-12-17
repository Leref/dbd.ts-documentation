---
description: Returns how many users are banned in the provided guild.
---

# $banCount
### Usage
```php
$banCount[guildID]
```

This function has one param.

| Param | Description | Type | Required |
| :--- | :--- | :--- | :--- |
| guildID | The guild to return the ban count for. | Snowflake | Yes |

### Example
```javascript
bot.commands.add({
    type: "basicCommand",
    name: "bans",
    code: `Ban Count: $banCount[$guildID]`
})
```

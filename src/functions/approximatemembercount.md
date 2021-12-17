---
description: Returns the approximate member count of provided guild.
---

# $approximateMemberCount
### Usage
```php
$approximateMemberCount[guildID]
```

This function has one param.

| Param | Description | Type | Required |
| :--- | :--- | :--- | :--- |
| guildID | The guild to return the approximate member count for. | Snowflake | Yes |

### Example
```javascript
bot.commands.add({
    type: "basicCommand",
    name: "members",
    code: `Members for Akarui Development: $approximateMemberCount[773352845738115102]`
})
```
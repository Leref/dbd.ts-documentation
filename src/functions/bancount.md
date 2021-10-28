---
description: Returns how many users are banned in the provided guild.
---

# $banCount
### Usage
```php
$banCount[guildID]
```

This function has one field.

| Field | Description | Type | Required |
| :--- | :--- | :--- | :--- |
| guildID | The guild to return the ban count for. | snowflake | yes |

### Example
```javascript
bot.commands.add({
    type: "basicCommand",
    name: "bans",
    code: `Ban Count: $banCount[$guildID]`
})
```

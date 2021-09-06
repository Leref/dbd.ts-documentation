---
description: Return approximate member count of given guild.
---

# $approximateMemberCount

### Usage

```php
$approximateMemberCount[guildID]
```

This function has one field.

| Field | Description | Type | Required |
| :--- | :--- | :--- | :--- |
| guildID | The guild to return the approximate member count for. | snowflake | yes |

### Example

```javascript
bot.commands.add({
    type: "basicCommand",
    name: "members",
    code: `Members for Akarui Development: $approximateMemberCount[773352845738115102]`
})
```




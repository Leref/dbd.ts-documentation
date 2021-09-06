---
description: Returns the guild ID that this channel belongs to.
---

# $channelGuildID
### Usage
```php
$channelGuildID or $channelGuildID[channelID]
```
This function has one field.

| Field | Description | Type | Required |
| :--- | :--- | :--- | :--- |
| channelID | The channel to return this data for. | snowflake | no |


### Example
```javascript
bot.commands.add({
    type: "basicCommand",
    name: "example",
    code: `$channelGuildID[775821524925022228]`
})
```

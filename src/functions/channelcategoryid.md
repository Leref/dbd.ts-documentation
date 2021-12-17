---
description: Returns the category ID that this channel is under.
---

# $channelCategoryID
### Usage
```php
$channelCategoryID or $channelCategoryID[channelID]
```
This function has one fields.

| Field | Description | Type | Required |
| :--- | :--- | :--- | :--- |
| channelID | The channel to return this data for. | Snowflake | No |


### Example
```javascript
bot.commands.add({
    type: "basicCommand",
    name: "example",
    code: `<#$channelID>'s Category: $channelCategoryID`
})
```
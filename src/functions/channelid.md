---
description: Returns the channel's ID.
---

# $channelID
### Usage
```php
$channelID or $channelID[channelName]
```
This function has one param.

| Param | Description | Type | Required |
| :--- | :--- | :--- | :--- |
| channelName | The channel name to return the channel ID for. **\*** | Snowflake | No |

**\*** If `channelName` isn't provided, then the current channel ID is returned.

### Example
```javascript
bot.commands.add({
    type: "basicCommand",
    name: "channel",
    code: `channelID: $channelID
    channelMentions: <#$channelID>
    channelName: $channelName`
})
```

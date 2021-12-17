---
description: Deletes the provided channels.
---

# $deleteChannels
### Usage
```php
$deleteChannels[channelIDs]
```

This function has one param.

| Param | Description | Type | Required |
| :--- | :--- | :--- | :--- |
| channelIDs | The channel IDs to delete, separated by `;`. | Snowflake | Yes |

### Example
```javascript
bot.commands.add({
  type: "basicCommand",
  name: "example",
  code: `$deleteChannels[$channelID]` //Deletes the current channel
})
```
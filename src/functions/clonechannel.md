---
description: Clones the provided channel.
---

# $cloneChannel
### Usage
```php
$cloneChannel[channelID;returnChannelID]
```
This function has two params.

| Param | Description | Type | Required |
| :--- | :--- | :--- | :--- |
| channelID | The channel to clone. | Snowflake | Yes |
| returnChannelID | Whether to return the ID of this newly cloned channel. | Boolean | No |

### Example
```javascript
bot.commands.add({
  type: "basicCommand",
  name: "clone",
  code: `New <#$channelID> Clone: <#$cloneChannel[$channelID;yes]>
  $onlyIf[$hasPerm[$guildID;$authorID;managechannels]==true;]`
})
```

---
description: Clones the provided channel.
---

# $cloneChannel

### Usage
```php
$cloneChannel[channelID;returnChannelID]
```
This function has two fields.

| Field | Description | Type | Required |
| :--- | :--- | :--- | :--- |
| channelID | The channel to clone. | snowflake | yes |
| returnChannelID | Whether to return the ID of this newly cloned channel. | boolean | no |

### Example
```js
bot.commands.add({
  type: "basicCommand",
  name: "clone",
  code: `New <#$channelID> Clone: <#$cloneChannel[$channelID;yes]>
  $onlyIf[$hasPerm[$guildID;$authorID;managechannels]==true;]`
})
```

---
description: Gets the slowmode of a channel in seconds, or 0 if there is no slowmode.
---

# $getChannelSlowmode
### Usage
```php
$getChannelSlowmode[channelID]
```

This function has one param.

| Param | Description | Type | Required
| :---- | :---- | :---- | :----
| channelID | The channel to get the slowmode of. | Snowflake | Yes

### Examples
**Example #1**
```javascript
bot.commands.add({
  type: "basicCommand",
  name: "example",
  code: `$getChannelSlowmode[$channelID]` //Returns the current channel's slowmode.
})
```

**Example #2**
```javascript
bot.commands.add({
  type: "basicCommand",
  name: "example",
  code: `$getChannelSlowmode[$mentionedChannels[1;yes]]` //Returns the mentioned channel's slowmode.
})
```
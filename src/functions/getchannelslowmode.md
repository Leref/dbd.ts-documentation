---
description: Gets the slowmode of a channel in seconds, or 0 if there is no slowmode.
---

# $getChannelSlowmode
### Usage
```php
$getChannelSlowmode[channelID]
```

| Field | Description | Type | Required
| :---- | :---- | :---- | :----
| channelID | The channel to get the slowmode of. | snowflake | yes

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
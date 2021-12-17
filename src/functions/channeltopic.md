---
description: Returns a channel's topic/description.
---
# $channelTopic
### Usage
```php
$channelTopic[channelID]
```

This function has one param.

| Param | Description | Type | Required
| :---- | :---- | :---- | :-----
| channelID | The channel to get the topic of. | Snowflake | Yes

### Examples
**Example #1**
```javascript
bot.commands.add({
    type: "basicCommand",
    name: "example",
    code: `$channelTopic[$channelID]` //Returns the topic of the current channel
})
```

**Example #2**
```javascript
bot.commands.add({
    type: "basicCommand",
    name: "example",
    code: `$channelTopic[$mentionedChannels[1;yes]]` //Returns the topic of the mentioned channel
})
```
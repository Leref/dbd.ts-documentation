---
description: Returns a channel's topic/description.
---
# $channelTopic
### Usage
```php
$channelTopic[channelID]
```

This function has one field.

| Field | Description | Type | Required
| :---- | :---- | :---- | :-----
| channelID | The channel to get the topic of. | snowflake | yes

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
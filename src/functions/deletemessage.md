---
description: Deletes a message from a channel.
---

# $deleteMessage
### Usage
```php
$deleteMessage[channelID;messageID]
```
This function has two params.

| Param | Description | Type | Required |
| :--- | :--- | :--- | :--- |
| channelID | The channel where the message is. | Snowflake | Yes
| messageID | The message to delete. | Snowflake | Yes

### Example
```javascript
bot.commands.add({
  type: "basicCommand",
  name: "example",
  code: `$deleteMessage[$mentionedChannels[1];$noMentionMessage]` //Usage: !command #channel <message id>
})
```
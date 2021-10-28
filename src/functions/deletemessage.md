---
description: Deletes a message from a channel.
---

# $deleteMessage
### Usage
```php
$deleteMessage[channelID;messageID]
```

### Example
```javascript
bot.commands.add({
  type: "basicCommand",
  name: "example",
  code: `$deleteMessage[$mentionedChannels[1];$noMentionMessage]` //Usage: !command #channel <message id>
})
```
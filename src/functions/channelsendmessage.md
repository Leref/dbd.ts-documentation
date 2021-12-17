---
description: Sends a message to desired channel and optionally returns the message ID.
---

# $channelSendMessage
### Usage
```php
$channelSendMessage[channelID;message;returnMessageID]
```
This function has three params.

| Param | Description | Type | Required |
| :--- | :--- | :--- | :--- |
| channelID | The channel to send this message to. | Snowflake | Yes |
| message | The message to send. | String | Yes |
| returnMessageID | Whether to return the message ID. | Boolean | No |

### Example
```javascript
bot.commands.add({
    type: "basicCommand",
    name: "send",
    code: `$channelSendMessage[$mentionedChannels[1;yes];Hello World!]`
})
```

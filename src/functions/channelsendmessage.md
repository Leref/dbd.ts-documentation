---
description: Sends a message to desired channel and optionally returns the message ID.
---

# $channelSendMessage
### Usage
```php
$channelSendMessage[channelID;message;returnMessageID]
```
This function has three field.

| Field | Description | Type | Required |
| :--- | :--- | :--- | :--- |
| channelID | The channel to send this message to. | snowflake | yes |
| message | The message to send. | string | yes |
| returnMessageID | Whether to return the message ID of the new message or not. | boolean | no |

### Example
```javascript
bot.commands.add({
    type: "basicCommand",
    name: "send",
    code: `$channelSendMessage[$mentionedChannels[1;yes];Hello World!]`
})
```

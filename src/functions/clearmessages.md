---
description: Clear messages from a channel.
---

# $clearMessages
### Usage
```php
$clearMessages[channelID;amount;returnDeletedMessageCount]
```
This function has three params.

| Param | Description | Type | Required |
| :--- | :--- | :--- | :--- |
| channelID | The channel to clear messages in. | Snowflake | Yes |
| amount | The amount of message to delete. | Integer | Yes
| returnDeletedMessageCount | Whether to return the actual amount of deleted messages. | Boolean | No |

### Example
```javascript
bot.commands.add({
  type: "basicCommand",
  name: "clear",
  code: `
  $onlyIf[$hasPerm[$guildID;$authorID;managemessages]==true;You need the manage_messages permission to use that!]
  Successfully purged \`$clearMessages[$channelID;$message;yes]\` messages.
  $onlyIf[$isNumber[$message]==true;Please provide how many messages to clear. Usage: \`!clear (amount)\`]`
})
```

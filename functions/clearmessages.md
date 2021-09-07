---
description: Clear messages from a channel.
---

# $clearMessages
### Usage
```php
$clearMessages[channelID;amount;returnDeletedMessageCount]
```
This function has three fields.

| Field | Description | Type | Required |
| :--- | :--- | :--- | :--- |
| channelID | The channel to clear messages in. | snowflake | yes |
| amount | The amount of message to delete. | integer | yes
| returnDeletedMessageCount | Whether to return the actual amount of deleted messages. | boolean | no |

### Example
```js
bot.commands.add({
  type: "basicCommand",
  name: "clear",
  code: `Successfully purged \`$clearMessages[$channelID;$message;yes]\` messages.
  $onlyIf[$isNumber[$message]==true;Please provide how many message to clear. Usage: \`!clear (amount)\`]
  $onlyIf[$hasPerm[$guildID;$authorID;managemessages]==true;You need the manage_messages permission to use that!]`
})
```

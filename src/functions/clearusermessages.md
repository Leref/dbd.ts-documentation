---
description: Clear messages by a user from the channel.
---

# $clearUserMessages
### Usage
```php
$clearUserMessages[channelID;userID;amount;returnDeletedMessageCount]
```
This function has four params.

| Param | Description | Type | Required |
| :--- | :--- | :--- | :--- |
| channelID | The channel to clear messages in. | Snowflake | Yes |
| userID | The user to clear messages for. | Snowflake | Yes |
| amount | The amount of message to delete. | Integer | Yes
| returnDeletedMessageCount | Whether to return the actual amount of deleted messages. | Boolean | No |

### Example
```javascript
bot.commands.add({
  type: "basicCommand",
  name: "clear-user",
  code: `
  $onlyIf[$mentioned[1]!=;Please mention someone. Usage: \`!clear (amount) (user)\`]
  $onlyIf[$isNumber[$message[1]]==true;Please provide how many message to clear. Usage: \`!clear (amount) (user)\`]
  $onlyIf[$hasPerm[$guildID;$authorID;managemessages]==true;You need the manage_messages permission to use that!]
  Successfully purged \`$clearUserMessages[$channelID;$mentioned[1];$message[1];Yes]\` messages by $userTag[$mentioned[1]].`
})
```

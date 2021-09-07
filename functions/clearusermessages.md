---
description: Clear messages by a user from the channel.
---

# $clearUserMessages
### Usage
```php
$clearUserMessages[channelID;userID;amount;returnDeletedMessageCount]
```
This function has four fields.

| Field | Description | Type | Required |
| :--- | :--- | :--- | :--- |
| channelID | The channel to clear messages in. | snowflake | yes |
| userID | The user to clear messages for. | snowflake | yes |
| amount | The amount of message to delete. | integer | yes
| returnDeletedMessageCount | Whether to return the actual amount of deleted messages. | boolean | no |

### Example
```js
bot.commands.add({
  type: "basicCommand",
  name: "clear-user",
  code: `Successfully purged \`$clearUserMessages[$channelID;$mentioned[1];$message[1];yes]\` messages by $userTag[$mentioned[1]].
  $onlyIf[$mentioned[1]!=;Please mention someone. Usage: \`!clear (amount) (user)\`]
  $onlyIf[$isNumber[$message[1]]==true;Please provide how many message to clear. Usage: \`!clear (amount) (user)\`]
  $onlyIf[$hasPerm[$guildID;$authorID;managemessages]==true;You need the manage_messages permission to use that!]`
})
```

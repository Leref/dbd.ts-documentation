---
description: Deletes the provided emojis.
---
# $deleteEmojis
### Usage
```php
$deleteEmojis[guildID;reason;emojiIDs]
```

This function has three params.

| Param | Description | Type | Required |
| :--- | :--- | :--- | :--- |
| guildID | The guild which these emoji(s) belong to. | Snowflake | Yes |
| reason | The reason for deleting these emoji(s). | String | No |
| emojiIDs | The emojis to delete, separated by `;`. | Snowflake | Yes

### Example
```javascript
bot.commands.add({
  type: "basicCommand",
  name: "example",
  code: `$deleteEmojis[$guildID;;<a:leref_dance:864243873361952778>]` //Deletes the leref_dance emoji
})
```
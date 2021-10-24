---
description: Deletes the provided emojis.
---
# $deleteEmojis
### Usage
```php
$deleteEmojis[guildID;reason;emojiIDs]
```

| Field | Description | Type | Required |
| :--- | :--- | :--- | :--- |
| guildID | The guild which these emoji(s) belong to. | snowflake | yes |
| reason | The reason for deleting these emoji(s). | string | no |
| emojiIDs | The emojis to delete, separated by `;`. | snowflake | yes

### Example
```php
bot.commands.add({
  type: "basicCommand",
  name: "example",
  code: `$deleteEmojis[$guildID;;<a:leref_dance:864243873361952778>]` //Deletes the leref_dance emoji
})
```

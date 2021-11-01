# $createTextChannel
### Usage
```php
$createTextChannel[guildID;type;name;categoryID;reason;returnChannelID;nsfw;slowmode;position]
```

This function has nine fields.


| Field | Description | Type | Required
| :--- | :--- | :--- | :--- |
| guildID | The guild to create this channel in. | snowflake | yes
| type | The text-based channel type. | [TextBasedChannel](/src/typedefs/textbasedchannel.md) | yes
| name | The name of this channel. | string | yes |
| categoryID | The category that this channel should belong to. | snowflake | no
| reason | The reason for creating this channel. | string | no |
| returnChannelID | Whether to return the newly created channel's ID. | boolean | no
| nsfw | Whether this channel should be marked as NSFW, only valid for regular text channels. | boolean | no
| slowmode | The slowmode for this channel. | time | no
| position | The position of this channel. | integer | no

### Example
```javascript
bot.commands.add({
    type: "basicCommand",
    name: "example",
    code: `$createTextChannel[$guildID;text;chat]`
})
```
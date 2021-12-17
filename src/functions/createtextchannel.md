# $createTextChannel
### Usage
```php
$createTextChannel[guildID;type;name;categoryID;reason;returnChannelID;nsfw;slowmode;position]
```

This function has nine params.


| Param | Description | Type | Required
| :--- | :--- | :--- | :--- |
| guildID | The guild to create this channel in. | Snowflake | Yes
| type | The text-based channel type. | [TextBasedChannel](/src/typedefs/textbasedchannel.md) | Yes
| name | The name of this channel. | String | Yes |
| categoryID | The category that this channel should belong to. | Snowflake | No
| reason | The reason for creating this channel. | String | No |
| returnChannelID | Whether to return the newly created channel's ID. | Boolean | No
| nsfw | Whether this channel should be marked as NSFW, only valid for regular text channels. | Boolean | No
| slowmode | The slowmode for this channel. | Time | No
| position | The position of this channel. | Integer | No

### Example
```javascript
bot.commands.add({
    type: "basicCommand",
    name: "example",
    code: `$let[channel;$createTextChannel[$guildID;text;chat;;;yes]]
    Created new channel <#$get[channel]>!`
})
```
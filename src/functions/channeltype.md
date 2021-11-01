---
description: Allows you to comment on your code, without the text being included in the bot's response.
---
# $channelType
### Usage
```php
$channelType[channelID]
```

This function has one field.

| Field | Description | Type | Required
| :---- | :---- | :---- | :-----
| channelID | The channel to get the type of. | snowflake | yes

### Examples
**Example #1**
```javascript
bot.commands.add({
    type: "basicCommand",
    name: "example",
    code: `$channelType[$channelID]` //Returns the current channel's type
})
```

**Example #2**
```javascript
bot.commands.add({
    type: "basicCommand",
    name: "example",
    code: `$channelType[$findChannel[$message]]` //Returns the channel type of the provided channel
})
```
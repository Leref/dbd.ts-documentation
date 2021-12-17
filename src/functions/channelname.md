---
description: Returns the channel's name.
---

# $channelName
### Usage
```php
$channelName or $channelName[channelID]
```
This function has one param.

| Param | Description | Type | Required |
| :--- | :--- | :--- | :--- |
| channelID | The channel ID to return the channel name for. **\*** | Snowflake | No |
**\*** If `channelID` isn't provided, then the current channel name is returned.

### Example
```javascript
bot.commands.add({
  type: "basicCommand",
  name: "example",
  code: `The current channel name is \`$channelName\``
})
```
![Result](https://user-images.githubusercontent.com/69215413/146600255-9dde9f4b-1b30-4338-b5f1-7dd022201bc8.png)
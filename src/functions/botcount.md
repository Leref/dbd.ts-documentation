---
description: Returns how many bots are in a server.
---
# $botCount
### Usage
```php
$botCount[guildID]
```
This function has one param.

| Param | Description | Type | Required
| :---- | :---- | :---- | :----
| guildID | The guild to get the bot for. | Snowflake | Yes

### Example
```javascript
bot.commands.add({
  type: "basicCommand",
  name: "example",
  code: `
  $fetchGuildMembers[$guildID] $ignoreCode[Fetching all guild members for a accurate count]
  This server has **$botCount bots**`
})
```
![Result](https://user-images.githubusercontent.com/69215413/146687437-99d3f1d1-54b9-4a87-b9ad-a9014a460286.png)

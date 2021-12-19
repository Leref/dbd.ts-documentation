---
description: Forces the bot to leave every server that is provided.
---
# $botLeave
### Usage
```php
$botLeave[guildID;...]
```
This function has one param.

| Param | Description | Type | Required
| :---- | :---- | :---- | :----
| guildID | The guild(s) to leave. | Snowflake | Yes

{% hint style="warning" %}
This function should be used with caution. You should limit use of it to the bot owner(s) only.
{% endhint %}

### Example
```javascript
bot.commands.add({
  type: "basicCommand",
  name: "example",
  code: `
  $onlyForIDs[$botOwnerID;You are not my bot owner!]
  Bye!
  $botLeave[$guildID]
  `
})
```

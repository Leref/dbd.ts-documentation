---
description: Returns whether or not the provided channel exists.
---

# $channelExists
### Usage
```php
$channelExists[channelID]
```
This function has one param.

| Param | Description | Type | Required |
| :--- | :--- | :--- | :--- |
| channelID | The channel to check. | Snowflake | No |

### Examples
**Example #1**
```javascript
bot.commands.add({
  type: "basicCommand",
  name: "example",
  code: `$channelExists[kwekdlwe]` //false
})
```

**Example #w**
```javascript
bot.commands.add({
  type: "basicCommand",
  name: "example",
  code: `$channelExists[919345931286110218]` //true
})
```
---
description: Checks whether the user is a bot.
---

# $isBot
### Usage
```php
$isBot[userID]
```

This function has one param.

| Param | Description | Type | Required
| :---- | :---- | :---- | :----
| userID | The user to check. | Snowflake | Yes

### Examples
**Example #1**
```javascript
bot.commands.add({
    type: "basicCommand",
    name: "example",
    code: `$isBot[$authorID]` //Returns whether or not the author is a bot
})
```

**Example #2**
```javascript
bot.commands.add({
    type: "basicCommand",
    name: "example",
    code: `$isBot[$mentioned[1]]` //Returns whether or not the mentioned user is a bot
})
```
---
description: Returns the bot owner's ID.
---

# $botOwnerID
### Usage
```php
$botOwnerID or $botOwnerID[separator]
```
This function has one param.

| Param | Description | Type | Required |
| :--- | :--- | :--- | :--- |
| separator | The separator between each team member, applicable if the owner of this bot is a team. | String | No |

### Example
```javascript
bot.commands.add({
    type: "basicCommand",
    name: "example",
    code: `$onlyForIDs[$botOwnerID;Only my owner can use that!]
Hello <@$botOwnerID>!`
})
```

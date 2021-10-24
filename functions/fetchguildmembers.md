---
description: Fetches members of a guild.
---
# $fetchGuildMembers
### Usage
```php
$fetchGuildMembers[guildID]
```
This function has one field.

| Field | Description | Type | Required |
| :--- | :--- | :--- | :--- |
| guildID | The guild to fetch the members of. | snowflake | yes

{% hint style="info" %} `$fetchGuildMembers` doesn't return any output. {% endhint %}

### Example
```javascript
bot.commands.add({
    type: "basicCommand",
    name: "example",
    code: `$fetchGuildMembers[$guildID]` //Fetches the current guild's members
})
```

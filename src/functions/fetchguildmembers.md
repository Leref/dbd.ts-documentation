---
description: Fetches and cahces members of a guild.
---

# $fetchGuildMembers
### Usage
```php
$fetchGuildMembers[guildID]
```
This function has one param.

| Param | Description | Type | Required |
| :--- | :--- | :--- | :--- |
| guildID | The guild to fetch the members of. | Snowflake | Yes

{% hint style="info" %} `$fetchGuildMembers[]` doesn't return any output. {% endhint %}
{% hint style="warning" %} It's highly recommended that you have the `GUILD_MEMBERS` intent enabled when using this function. {% endhint %}

### Example
```javascript
bot.commands.add({
    type: "basicCommand",
    name: "example",
    code: `$fetchGuildMembers[$guildID]` //Fetches the current guild's members
})
```

---
description: Creates and returns a server's invite URL.
---

# $getServerInvite
### Usage
```php
$getServerInvite[guildID]
```

This function has one param.

| Param | Description | Type | Required
| :---- | :---- | :---- | :----
| guildID | The server to create the invite in. | Snowflake | Yes


{% hint style="warning" %}
Your bot must have the `CREATE_INSTANT_INVITE` permission in the provided guild for this function to work.
{% endhint %}

### Example
```javascript
bot.commands.add({
    type: "basicCommand",
    name: "example",
    code: `$getServerInvite[$guildID]` //Returns the current server's invite
})
```
---
description: Sets a cooldown.
---

# $cooldown
### Usage
```php
$cooldown[id;time;errorMessage]
```

This function has three fields.

| Field | Description | Type | Required |
| :--- | :--- | :--- | :---
| id | The user, channel, or guild to assign this cooldown to. | snowflake | yes
| duration | How long the cooldown should last. | time | yes |
| errorMessage | The message to return when the cooldown is ongoing. | string | no

{% hint style="info" %} You can use `$get[time_left]` in 'errorMessage' to get how much time is left on the cooldown. {% endhint %}

### Examples
**Creating a Global User Cooldown:**
```
$cooldown[$authorID;1h;You have to wait $get[time_left] to use this command again!]
```

**Creating a Local User Cooldown:**
```
$cooldown[$guildID_$authorID;1h;You have to wait $get[time_left] to use this command again!]
```

**Creating a Channel Cooldown:**
```
$cooldown[$channelID;1h;You have to wait $get[time_left] to use that command in this channel!]
```

**Creating a Guild Cooldown:**
```
$cooldown[$guildID;1h;You have to wait $get[time_left] to use that command in this channel!]
```
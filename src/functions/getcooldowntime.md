---
description: Gets how much time is left on a cooldown, in milliseconds.
---
# $getCooldownTime
### Usage
```php
$getCooldownTime[commandName;id]
```

This function has two params.

| Param | Description | Type | Required
| :--- | :--- | :--- | :---
| commandName | The command to get the cooldown from. | String | Yes
| id | The same thing you provided for 'id' in [$cooldown](./cooldown.md). | Snowflake | Yes

{% hint style="info" %} `$getCooldownTime` returns `0` if there is no cooldown active for the provided `commandName` on `id`. {% endhint %} 

### Example
```javascript
bot.commands.add({
  type: "basicCommand",
  name: "example",
  code: `$getCooldownTime[someCommandName;$authorID]` //Returns how much time is left on 'someCommandName' cooldown in milliseconds
  })
```
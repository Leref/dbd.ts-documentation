---
description: Returns a user's badges.
---

# $getUserBadges
### Usage
```php
$getUserBadges or $getUserBadges[userID;separator]
```

This function has two fields.

| Field | Description | Type | Required |
| :--- | :--- | :--- | :--- |
| userID | The user to get the badges for. | snowflake | no
| separator | The separator between each badge, commas by default. | string | no

{% hint style="info" %} Nitro/paid badges generally are excluded. {% endhint %}

The output of `$getUserBadges` looks like this: `DISCORD_EMPLOYEE, PARTNERED_SERVER_OWNER, HYPESQUAD_EVENTS, BUG_HUNTER_LEVEL_1, HOUSE_BRAVERY, HOUSE_BRILLIANCE, HOUSE_BALANCE, EARLY_SUPPORTER, BUG_HUNTER_LEVEL_2, VERIFIED_BOT, EARLY_VERIFIED_BOT_DEVELOPER, DISCORD_CERTIFIED_MODERATOR`

### Examples
#### Example #1
```javascript
bot.commands.add({
    type: "basicCommand",
    name: "example",
    code: `$getUserBadges` //Returns the author's badges.
```

#### Example #2
```javascript
bot.commands.add({
    type: "basicCommand",
    name: "example",
    code: `$getUserBadges[$mentioned[1;yes]]` //Returns the mentioned user'sadges.
```
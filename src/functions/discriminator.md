---
description: Returns the discriminator (last four digits of their tag) of the given user.
---

# $discriminator
### Usage
```php
$discriminator or $discriminator[userID]
```

This function has one param.

| Param | Description | Type | Required |
| :--- | :--- | :--- | :--- |
| userID | The user to get the discriminator from. **\*** | Snowflake | No |
**\*** Returns author's discriminator if no `userID` is provided.

### Examples
**Example #1**
```javascript
bot.commands.add({
    type: "basicCommand",
    name: "example",
    code: `$discriminator` //Returns the author's discriminator
})
```

**Example #2**
```javascript
bot.commands.add({
    type: "basicCommand",
    name: "example",
    code: `$discriminator[608358453580136499]` //Returns Leref's discriminator (0001)
})
```

**Example #3**
```javascript
bot.commands.add({
    type: "basicCommand",
    name: "example",
    code: `$discriminator[$mentioned[1;yes]]` //Returns the mentioned user's discriminator
})
```
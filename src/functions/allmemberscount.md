---
description: Returns the total amount of members from every guild your bot is in.
---

# $allMembersCount

### Usage

```php
$allMembersCount
```

### Example

```javascript
bot.commands.add({
    type: "basicCommand",
    name: "members",
    code: `Total Members: $allMembersCount`
})
```


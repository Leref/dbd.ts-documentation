---
description: Returns the ID of the user who ran this command.
---

# $authorID
## Usage
```php
$authorID
```

## Example
```javascript
bot.commands.add({
    name: "id",
    code: `Your ID is \`$authorID\``
})
```
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
![Result](https://user-images.githubusercontent.com/69215413/146599306-80abff87-2d74-4d14-9336-275577c9d584.png)
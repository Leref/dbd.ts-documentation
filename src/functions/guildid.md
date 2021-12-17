---
description: Returns the current guild's ID.
---

# $guildID
### Usage
```php
$guildID
```

### Example
```javascript
bot.commands.add({
  type: "basicCommand",
  name: "example",
  code: `This guild ID is $guildID`
})
```
![Result](https://user-images.githubusercontent.com/69215413/146605524-e0de1d2a-602d-4be6-8670-52c2f801bfd1.png)
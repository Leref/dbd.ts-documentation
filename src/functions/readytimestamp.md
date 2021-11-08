---
description: Returns the timestamp when the client was last ready, in milliseconds.
---

# $readyTimestamp
### Usage
```php
$readyTimestamp
```

### Example
```javascript
bot.commands.add({
    type: "basicCommand",
    name: "example",
    code: `I've been online since <t:$round[$divide[$readyTimestamp;1000];0]:f> (<t:$round[$divide[$readyTimestamp;1000];0]:R>)!`
})
```
![Result](https://user-images.githubusercontent.com/69215413/139557335-5ede3c79-5a70-4086-a631-cddd6c593dda.png)
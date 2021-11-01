---
description: Returns the name of the package.
---

# $packageName
### Usage
```php
$packageName
```

### Example
```javascript
bot.commands.add({
    type: "basicCommand",
    name: "example",
    code: `$packageName` //Returns "dbd.ts"
})
```
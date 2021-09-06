---
description: Adds reactions to the author's message.
---

# $addCmdReactions

### Usage

```php
$addCmdReactions[emoji(s)]
```

This function has one field.

1. `emoji(s)` - The emojis to react with, separate emojis using `;`. \| Required

### Examples

```javascript
bot.commands.add({
    type: "basicCommand",
    name: "react",
    code: `$addCmdReactions[✔]`
})
```

```javascript
bot.commands.add({
    type: "basicCommand",
    name: "react",
    code: `$addCmdReactions[🎉;✔]`
})
```


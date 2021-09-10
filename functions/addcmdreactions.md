---
description: Adds reactions to the author's message.
---

# $addCmdReactions

### Usage

```php
$addCmdReactions[emoji(s)]
```

This function has one field.

| Field | Description | Type | Required |
| :--- | :--- | :--- | :--- |
| emoji(s) | The emojis to react with, separate emojis using `;`. | string | yes |

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

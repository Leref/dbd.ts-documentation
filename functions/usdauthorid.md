---
description: Returns the ID of the user who ran the command.
---

# $authorID

This function returns the author's ID 

*The one who ran the command*

#### Usage

```javascript
$authorID
```

#### Example Usage

```javascript
bot.command({
    name: "id",
    code: `Your ID is \`$authorID\``
});
```
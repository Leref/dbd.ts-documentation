---
description: Archives a thread.
---

# $archiveThread
### Usage
```php
$archiveThread[threadID]
```

This function has one param.

| Parmas | Description | Type | Required |
| :--- | :--- | :--- | :--- |
| threadID | The ID of the thread channel to delete. | Snowflake | Yes |

### Example
```javascript
bot.commands.add({
  type: "basicCommand",
  name: "example",
  code: `
    $onlyIf[$channelType[$noMentionMessage]==thread;:x: That's a not a thread channel!]
    $archiveThread[$noMentionMessage]
    Archived thread!
  `
})

```
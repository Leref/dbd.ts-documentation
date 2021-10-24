---
description: Adds a member to the thread.
---

# $addThreadMember

### Usage

```php
$addThreadMember[guildID;threadID;userID;reason]
```

This function has four fields.

| Fields | Description | Type | Required |
| :--- | :--- | :--- | :--- |
| guildID | The guild that this thread channel belongs to. | snowflake | yes |
| threadID | The thread to add this user to. | snowflake | yes |
| userID | The user to add to this thread. | snowflake | yes |
| reason | The reason for adding this user to the thread. | string | no |


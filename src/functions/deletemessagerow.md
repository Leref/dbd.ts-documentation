---
description: Deletes specific row of components from a message.
---

# $deleteMessageRow
### Usage
```php
$deleteMessageRow[channelID;messageID;rowIndex]
```

This function has three params.

| Param | Description | Type | Required |
| :--- | :--- | :--- | :--- |
| channelID | The channel where this message was sent in. | Snowflake | Yes |
| messageID | The message to delete components row from. | Snowflake | Yes |
| rowIndex | The row to delete. | Integer | Yes |
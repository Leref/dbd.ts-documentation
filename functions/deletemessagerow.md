---
description: Deletes specific row of components from a message.
---
# $deleteMessageRow
### Usage
```php
$deleteMessageRow[channelID;messageID;rowIndex]
```

This function has three fields.

| Field | Description | Type | Required |
| :--- | :--- | :--- | :--- |
| channelID | The channel where this message was sent in. | snowflake | yes |
| messageID | The message to delete components row from. | snowflake | yes |
| rowIndex | The row to delete. | integer | yes |

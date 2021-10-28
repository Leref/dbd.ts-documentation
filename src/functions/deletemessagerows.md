---
description: Deletes all components from a message.
---

# $deleteMessageRows
### Usage
```php
$deleteMessageRows[channelID;messageID]
```
This function has two fields.

| Field | Description | Type | Required |
| :--- | :--- | :--- | :--- |
| channelID | The channel where this message was sent. | snowflake | yes |
| messageID | The message to delete the components for. | snowflake | yes |

---
description: Deletes all components from a message.
---

# $deleteMessageRows
### Usage
```php
$deleteMessageRows[channelID;messageID]
```
This function has two params.

| Field | Description | Type | Required |
| :--- | :--- | :--- | :--- |
| channelID | The channel where this message was sent. | Snowflake | Yes |
| messageID | The message to delete the components for. | Snowflake | Yes |

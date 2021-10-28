---
description: Edits a existing message.
---

# $editMessage
### Usage
```php
$editMessage[channelID;messageID;content]
```
This function has three fields.

| Field | Description | Type | Required
| :---- | :---- | :---- | :----
| channelID | The channel that this message belongs to. | snowflake | yes
| messageID | The message to edit. | snowflake | yes
| content | The new contents of this message. | string | yes
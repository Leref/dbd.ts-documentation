---
description: Adds a attachment to the bot's response.
---

# $attachment

### Usage

```php
$attachment[url;name.extension]
```

This function has two fields.

| Fields | Description | Type | Required |
| :--- | :--- | :--- | :--- |
| url | The URL of this attachment. | string | yes |
| name.extension | The name and extension of this attachment. | string | no |

### Example

```javascript
bot.commands.add({
    type: "basicCommand",
    name: "attachment",
    code: `$attachment[https://imgur.com/eZfedQF.png;image.png]`
})
//The URL must end with a extension, else it is sent as a unpreviewable file.
```

![Output](../.gitbook/assets/image%20%281%29.png)




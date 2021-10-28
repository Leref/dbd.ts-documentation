---
description: Returns the avatar URL of the user who ran this command.
---

# $authorAvatar
### Usage
```php
$authorAvatar or $authorAvatar[size;dynamic]
```
This function has two fields.

| Field | Description | Type | Required |
| :--- | :--- | :--- | :--- |
| size | The size to display this avatar as. | string [(ImageSize)](typedefs/imagesizes.md) | no |
| dynamic | Whether to change the image to a GIF for animated avatars. | boolean | no |

### Example
```javascript
bot.commands.add({
    type: "basicCommand",
    name: "avatar",
    code: `$image[$authorAvatar[4096;yes]]`
})
```

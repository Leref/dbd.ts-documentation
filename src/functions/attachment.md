---
description: Adds a attachment to the bot's response.
---

# $attachment
### Usage
```php
$attachment[URL;name.extension]
```

This function has two params.

| Param | Description | Type | Required |
| :--- | :--- | :--- | :--- |
| URL | The URL of this attachment. | String | Yes |
| name.extension | The name and extension of this attachment. | String | No |

{% hint style="danger" %}
The 'URL' must end with a extension, else it is sent as a unpreviewable file.
{% endhint%}

### Example
```javascript
bot.commands.add({
    type: "basicCommand",
    name: "attachment",
    code: `$attachment[https://imgur.com/eZfedQF.png;image.png]`
})
```
![Result](https://user-images.githubusercontent.com/69215413/132230947-4ef1d689-da5d-4f74-90ba-5a9a03ed980d.png)
---
description: Adds reactions to the author's message.
---

# $author

## Usage

```php
$author[index;text;icon;url]
```

This function has four fields.

| Field | Description | Type | Required |
| :--- | :--- | :--- | :--- |
| index | The embed to add this author to. | integer | yes |
| text | The author text. | string | yes |
| icon | The author icon URL. | string | no |
| url | The author hyperlink URL. | string | no |

## Example
```javascript
bot.commands.add({
    type: "basicCommand",
    name: "author",
    code: `$author[1;Author Text;$authorAvatar;https://google.com]
    $description[1;⬆️ That is the author.]`
})
```
![Result](https://user-images.githubusercontent.com/69215413/132242363-edc21242-ddda-4894-8178-36a04369a1d9.png)

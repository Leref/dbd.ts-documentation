---
description: Sets an embed's footer.
---

# $footer
### Usage
```php
$footer[index;text;iconURL]
```

This function has three params.

| Param | Description | Type | Required |
| :--- | :--- | :--- | :--- |
| index | The embed to add this footer to. | Integer | Yes |
| text | The footer text. | String | Yes |
| iconURL | The footter icon URL. | String | No |

### Example
```javascript
bot.commands.add({
    type: "basicCommand",
    name: "example",
    code: `$footer[Footer Text;$authorAvatar]
    $description[1;⬇️ That is the footer.]`
})
```
![Result](https://user-images.githubusercontent.com/69215413/138784258-dc175268-3501-4f38-a5c2-6c703a0ca000.png)
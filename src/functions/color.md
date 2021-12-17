---
description: Sets the embed's border color.
---

# $color
### Usage
```php
$color[index;colorHex]
```
This function has two params.

| Param | Description | Type | Required |
| :--- | :--- | :--- | :--- |
| index | The embed index that this color should belong to. | integer | yes |
| colorHex | The color hex of this embed color. | string | yes |

{% hint style="success" %}
Find color hexes [here](https://htmlcolorcodes.com/color-picker)!
{% endhint %}

### Example
```javascript
bot.commands.add({
    type: "command",
    name: "example",
    code: `$description[1;Hello World!]
    $color[1;ff57e0]`
})
```

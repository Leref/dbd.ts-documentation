---
description: Sets a embed's description.
--
# $description
### Usage
```php
$description[index;text]
```

This function has two fields.

| Field | Description | Type | Required
| :---- | :---- | :---- | :----
| index | The index of the embed to add thsi description to. | integer | yes
| text | The text that the description should contain. | string | yes

### Example
```javascript
bot.commands.add({
  type: "basicCommand",
  name: "example",
  code: `$description[1;This is a description!]`
})
```
![Result](https://user-images.githubusercontent.com/69215413/138605956-a84c322a-2ab1-40b9-85ba-c281062a7bd4.png)
---
description: Attaches a txt file to the bot's response.
---

# $createFile
### Usage
```php
$createFile[text;name]
```

This function has two fields.

| Field | Description | Type | Required |
| :--- | :--- | :--- | :---
| text | The text that the file should contain. | string | yes
| name | The file's name. | string | yes


### Example
```javascript
bot.commands.add({
  type: "basicCommand",
  name: "example",
  code: `$createfile[Hello World!;text]`
})
```
![](https://user-images.githubusercontent.com/69215413/139559552-bd3ec30d-caf4-40a5-b9ad-51437ae3f0b7.png)
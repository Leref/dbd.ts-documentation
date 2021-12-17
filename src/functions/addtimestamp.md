---
description: Adds a timestamp to the embed.
---

# $addTimestamp
### Usage
```php
$addTimestamp[index;ms]
```

This function has two params.

| Param | Description | Type | Required
| :---- | :---- | :---- | :----
| index | Index of the embed to add this timestamp to. | Integer | Yes
| ms | The milliseconds to set the timestamp to (current time by default). | Integer | No

### Example
```javascript
bot.commands.add({
  type: "basicCommand",
  name: "example",
  code: `$description[1;This embed has a timestamp!]
$addTimestamp[1]`
})
```
![Result](https://user-images.githubusercontent.com/69215413/138597772-e1e5d30f-86ee-4c13-950c-53d710400de7.png)
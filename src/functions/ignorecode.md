---
description: Allows you to comment on your code, without the text being included in the bot's response.
---
# $ignoreCode
### Usage
```php
$ignoreCode[text]
```

This function has one field.

| Field | Description | Type | Required
| :---- | :---- | :---- | :-----
| text | The text/code to ignore. | string | yes

### Example
```javascript
bot.commands.add({
    type: "basicCommand",
    name: "example",
    code: `Hello World! $ignoreCode[You will not see this in the bot's response]`
})
```
![Result](https://user-images.githubusercontent.com/69215413/139556001-a5158374-5ab5-4572-9308-6dbd431f70fe.png)
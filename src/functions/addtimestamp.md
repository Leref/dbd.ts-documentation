# $addTimestamp
### Usage
```php
$addTimestamp[index;ms]
```

This function has two fields.

| Field | Description | Type | Required
| :---- | :---- | :---- | :----
| index | Index of the embed to add this timestamp to. | integer | yes
| ms | The milliseconds to set the timestamp to (current time by default). | integer | no

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
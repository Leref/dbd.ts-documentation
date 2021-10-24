# $delete
Deletes a temporary variable that was set with [`$let[]`](./let.md).

### Usage
```php
$delete[variableName]
```
This function has one field.
| Field | Description | Type | Required |
| :--- | :--- | :--- | :--- |
| variableName | The temporary variable to delete. | string | yes |

### Example
```js
bot.commands.add({
  type: "basicCommand",
  name: "example",
  code: `$let[text;Hello!]
$get[text]
$delete[text]`
})
```

---
description: Adds a new field to this embed.
---

# $addField
### Usage
```php
$addField[embedIndex;text;value;inline]
```

This function has four params.

| Param | Description | Type | Required
| :---- | :---- | :---- | :----
| embedIndex | The embed that this field should belong to. | Integer | Yes
| name | The name of this field. | String | Yes
| value | The value of this field. | String | Yes
| inline | Whether fields should be inline. **\*** | Boolean | No
**\*** If 'yes', field will appear in inlined. However, if you have more than 3 fields \(or the fields are just too long\) with inline enabled, the bot will return rows with 3 fields \(2 if there is a thumbnail\) in each row. Inline fields will appear uninlined on mobile devices due to viewport size. 'no' by default.

### Examples
**Example #1**
```javascript
bot.commands.add({
    type: "basicCommand",
    name: "fields",
    code: `$addField[1;Name;Value]
    $addField[1;Name;Value]
    $addField[1;Name;Value]`
})
// Without Inline
```
![](https://user-images.githubusercontent.com/69215413/146597027-f6be6640-0003-4775-90ff-f720ca7bc663.png)

**Example #2**
```javascript
bot.commands.add({
    type: "basicCommand",
    name: "fields",
    code: `$addField[1;Name;Value;yes]
    $addField[1;Name;Value;yes]
    $addField[1;Name;Value;yes]`
})
// With Inline
```
![](https://user-images.githubusercontent.com/69215413/146597126-4f49c136-9924-4503-99c6-9c1b1f9fc47c.png)
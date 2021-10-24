---
description: Adds a new field to this embed.
---

# $addField

### Usage

```php
$addField[index;text;value;inline]
```

This function has four fields.

1. `index` - The embed index that this field should belong to. There can be up to ten embeds per message. \| Required
2. `name` - The name of this field. \| Required
3. `value` - The value of this field. \| Required
4. `inline` - If 'yes', field will appear in inlined. However, if you have more than 3 fields \(or the fields are just too long\) with inline enabled, the bot will return rows with 3 fields \(2 if there is a thumbnail\) in each row. 'no' by default. \| Optional

### Example

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


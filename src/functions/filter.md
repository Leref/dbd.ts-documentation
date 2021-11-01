---
description: Removes are phrases matching the provided 'queries' within 'text'.
---

# $filter
### Usage
```php
$filter[text;queries]
```

This function has two fields.

| Field | Description | Type | Required
| :--- | :--- | :--- | :---
| text | The text to filter. | string | yes
| queries | The phrases to remove from 'text', separated by `;`. | string | yes

### Examples
**Example #1**
```javascript
bot.commands.add({
    type: "basicCommand",
    name: "example",
    code: `$filter[Hello World!;Hello]` //Returns "World!"
})
```
**Example #2**
```javascript
bot.commands.add({
    type: "basicCommand",
    name: "example",
    code: `$filter[hi, how are you?;hi, ]` //Returns "how are you?"
})
```
---
description: Removes are phrases matching the provided 'queries' within 'text'.
---

# $filter
### Usage
```php
$filter[text;queries;...]
```

This function has two params.

| Param | Description | Type | Required
| :--- | :--- | :--- | :---
| text | The text to filter. | String | Yes
| queries | The phrases to remove from 'text'. | String | Yes

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
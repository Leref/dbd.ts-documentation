---
description: Formats provided milliseconds into a readable date.
---

# $formatMS
### Usage
```php
$formatMS[milliseconds;format]
```

This function has two params.

| Field | Description | Type | Required
| :---- | :---- | :---- | :----
| milliseconds | The milliseconds to format. | Integer | Yes
| format | The format to apply. | String | No

### Examples
**Example #1**
```javascript
bot.commands.add({
    type: "basicCommand",
    name: "example",
    code: `$formatMS[$getTimestamp]` //Returns the current date. For example, October 25th 2021.
})
```

**Example #2**
```javascript
bot.commands.add({
    type: "basicCommand",
    name: "example",
    code: `$formatMS[$getTimestamp;October 25th 2021, 11:39:50 pm]` //Returns the current date. For example, October 25th 2021, 11:39:50 pm.
})
```

**Example #3**
```javascript
bot.commands.add({
    type: "basicCommand",
    name: "example",
    code: `$formatMS[$getTimestamp;l]` //Returns the current date. For example, 10/25/2021.
})
```

**Example #4**
```javascript
bot.commands.add({
    type: "basicCommand",
    name: "example",
    code: `$formatMS[$getTimestamp;LLL]` //Returns the current date. For example, October 25, 2021 11:43 PM.
})
```

**Example #5**
```javascript
bot.commands.add({
    type: "basicCommand",
    name: "example",
    code: `$formatMS[$getTimestamp;MMM Do YY]` //Returns the current date. For example, Oct 25th 21.
})
```

**Example #6**
```javascript
bot.commands.add({
    type: "basicCommand",
    name: "example",
    code: `$formatMS[$getTimestamp;dddd]` //Returns the current day. For example, Monday.
})
```

<mark style="color:blue;">Find more information about formating <mark style="color:red;">[here](https://momentjs.com/)</mark>.</mark>
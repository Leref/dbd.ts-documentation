---
description: Removes all reactions from the provided message.
---
# $clearAllReactions
### Usage
```php
$clearAllReactions[channelID;messageID]
```

This function has two params.

| Param | Description | Type | Required
| :---- | :---- | :---- | :-----
| channelID | The channel where message is located. | Snowflake | Yes
| messageID | The message to remove reactions from. | Snowflake | Yes

### Example
```javascript
bot.commands.add({
    type: "basicCommand",
    name: "example",
    code: `$clearAllReactions[876920205526319144;904091144579850251]`
})
```

**Before:**\
![](https://user-images.githubusercontent.com/69215413/139556362-ab29b9bf-0596-4174-9bf5-57cd5cee2598.png)

**After:**\
![](https://user-images.githubusercontent.com/69215413/139556380-aa596c84-cdef-4112-8a41-68ecf708462f.png)
---
description: Fetches a temporary variable's current value.
---

# $get
### Usage
```php
$get[variableName]
```

This function has one param.

| Param | Description | Type | Required |
| :--- | :--- | :--- | :--- |
| variableName | The variable to get the value for. | String | Yes

### Example
```javascript
bot.commands.add({
  type: "basicCommand",
  name: "example",
  code: `$let[msgid;$channelSendMessage[$channelID;Hello World!;yes]]
$setTimeout[5s;$editMessage[$channelID;$get[msgid];Hi Planet!]]`
})
```

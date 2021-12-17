---
description: Edits an existing message.
---

# $editMessage
### Usage
```php
$editMessage[channelID;messageID;content]
```
This function has three params.

| Param | Description | Type | Required
| :---- | :---- | :---- | :----
| channelID | The channel that this message belongs to. | Snowflake | Yes
| messageID | The message to edit. | snowflake | Yes
| content | The new contents of this message. | String | Yes

### Example
```javascript
bot.commands.add({
  type: "basicCommand",
  name: "example",
  code: `
    $let[msgid;$makeReturn[
      $channelSendMessage[$channelID;
        $title[1;Hello World!]
        $color[1;GREEN]
        $description[1;Hello, how are you?]
      ;yes]
    ]]

    $setTimeout[5s;
      $editMessage[$channelID;$get[msgid];
        $title[1;DBD.TS]
        $description[1;DBD.TS is epic!]
        $color[1;BLUE]
      ]
    ]
  `
})
```

**Before:**\
![](https://user-images.githubusercontent.com/69215413/146604375-eda58232-fbbf-4424-8c2c-836c7c94d4e4.png)

**After 5 Seconds:**\
![](https://user-images.githubusercontent.com/69215413/146604376-fa227d07-d8ac-4fba-b352-8a6b647982b7.png)
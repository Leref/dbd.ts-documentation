---
description: Edits all rows/components for the provided message. 
---

# $editMessageRows
### Usage
```php
$editMessageRows[channelID;messageID;components]
```

This function has three params.

| Param | Description | Type | Required
| :---- | :---- | :---- | :----
| channelID | The channel where the message was sent. | Snowflake | Yes
| messageID | The message to edit the components for. | Snowflake | Yes
| components | The new rows/components for this message. | String | Yes 

### Example
```javascript
bot.commands.add({
  type: "basicCommand",
  name: "example",
  code: `$editMessageRows[$channelID;12345678901234678;
            $addActionRow
            $addButton[some_button;some button;primary]
            $addActionRow
            $addSelectMenu[some_menu;a menu!;1;1]
            $addSelectMenuOption[option 1;choose me.;option_1]
  ]`
})
```
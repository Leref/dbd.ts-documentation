---
description: Edits all rows/components for the provided message. 
---
# $editMessageRows
### Usage
```php
$editMessageRows[channelID;messageID;components]
```

This function has three fields.

| Field | Description | Type | Required
| :---- | :---- | :---- | :----
| channelID | The channel where the message was sent. | snowflake | yes
| messageID | The message to edit the components for. | snowflake | yes
| components | The new rows/components for this message. | string | yes 
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
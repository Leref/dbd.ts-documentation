---
description: Adds a new action row.
---
# $addActionRow
### Usage
```php
$addActionRow
```

{% hint style="info" %}
To add buttons/select menus to a command, you must first add a action row by using this function. You can create a new row by using this function again later in the code.
{% endhint %}

### Example
```javascript
bot.commands.add({
  type: "basicCommand",
  name: "example",
  code: `   
  $addActionRow
  $addButton[some_button;some button;primary]
  $addSelectMenu[some_menu;a menu!;1;1]
  $addSelectMenuOption[option 1;choose me.;option_1]
  
  $addActionRow $ignoreCode[New row gets added, buttons/select menu will appear under this row until addActionRow is used again]
  $addButton[some_button2;some button;primary]
  $addSelectMenu[some_menu2;a menu!;1;1]
  $addSelectMenuOption[option 2;choose me.;option_2]
`
})
```
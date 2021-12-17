---
description: Adds a select menu to this action row.
---
# $addSelectMenu
### Usage
```php
$addSelectMenu[customID;placeholder;minValues;maxValues;disabled]
```

This function has five parms.

| Param | Description | Type | Required |
| :--- | :--- | :--- | :--- |
| customID | The customID of this select menu. | String | Yes |
| placeholder | The select menu's placeholder. | String | Yes |
| minValues | The minimum amount of options that the user can select. | Integer | Yes |
| maxValues | The maximum amount of options that the user can select. | Integer | Yes |
| disabled | Whether this select menu should be disabled or not. | Boolean | Yes |

{% hint style="warning" %}
* Select menus must be sent inside an action row \(refer to [$addActionRow](./addactionrow.md)\).
* An action row can contain only one select menu.
* An action row containing a select menu cannot also contain buttons.
{% endhint %}

{% hint style="success" %}
Don't forget to add the `onInteraction` event to your main file. For example:

```javascript
bot.addEvent([
    "onMessage",
    "onInteraction" //This is what you need to add
])
```
{% endhint %}

### Example
```javascript
bot.commands.add({
    type: "basicCommand",
    name: "menu", 
    code: `A menu!
    $addActionRow
    $addSelectMenu[menu_1;Hi;1;1]
    $addSelectMenuOption[hi;im uwu;hi]
    $addSelectMenuOption[fiction;nice stuff;fiction]`
})

bot.commands.add({    
    type: "selectMenuCommand",
    code: `Interaction Value: $interactionValues | Interaction ID: $interactionID`
})
```

{% hint style="info" %}
[Click here](./addselectmenuoption.md) for more info about`$addSelectMenuOption[]`
{% endhint %}
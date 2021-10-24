# Author-Only Interactions
This article answers the frequently asked question "How do I make it so only the author can use button(s)/select menu(s)".

{% hint style="info" %} Adding `$authorID` to the `customID` (for buttons) or `value` (for select menus) fields makes it so you can check if the author is using the interaction or not with if statements. {% endhint %}

#### Buttons Example
Using `$addButton[]`:
```js
bot.commands.add({
  type: "basicCommand",
  name: "button",
  code: `$addActionRow
  Button!
  $addButton[button1_$authorID;Click Me OwO;primary]`
})
```

Replying to the Interaction:
```js
bot.commands.add({
  type: "buttonCommand",
  code: `$if[$interactionID==button1_$authorID;$updateInteraction
Hello World!
;$if[$includes[$interactionID;button1]==true;:x: You're not the author of this button! $ephemeral;]]`
})
```
{% hint style="danger" %} The 'name' property for the `buttonCommand` type shall not be used for author-only buttons. {% endhint %}

#### Select Menu Example
Using `$addSelectMenu[]`/`$addSelectMenuOption[]`:
```js
bot.commands.add({
  type: "basicCommand",
  name: "select",
  code: `Make a selection
$addActionRow
$addSelectMenu[menu1;select;1;0;no]
$addSelectMenuOption[Option 1;Hello World!;option1_$authorID]
$addSelectMenuOption[Option 2;Hello Planet!;option2_$authorID]`
})
```

Replying to the Interaction:
```js
bot.commands.add({
  type: "selectMenuCommand",
  name: "menu1",
  code: `$if[$interactionValues==option1_$authorID;$updateInteraction
Hello World!
;$if[$includes[$interactionValues;option1]==true;:x: You're not the author of this select menu! $ephemeral;]]

$if[$interactionValues==option2_$authorID;$updateInteraction
Hello Planet!
;$if[$includes[$interactionValues;option2]==true;:x: You're not the author of this select menu! $ephemeral;]]`
})
```

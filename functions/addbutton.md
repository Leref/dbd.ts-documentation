---
description: Adds a button to this action row.
---

# $addButton

### Usage
```
$addButton[customID/link;label;style;emoji;disabled (yes/no)]
```

This function has five fields.

| Field | Description | Type | Required |
| :--- | :--- | :--- | :--- |
| customID/link | The customID or link of this button. | string | yes |
| label | The label that this button displays. | string | yes |
| style | The style of this button. | string [(ButtonStyle)](typedefs/buttonstyles.md) | yes |
| emoji | The emoji that will appear to the left of the `label`, leave empty for no emoji. | string | no |
| disabled | Whether this button should be disabled or not. | boolean | yes

{% hint style="info" %}
There can be up to 5 buttons per action row.
{% endhint %}

### Example

Link Button:
```javascript
bot.commands.add({
    type: "basicCommand",
    name: "linkbutton",
    code: `Use DBD.TS!
$addActionRow
$addButton[https://npmjs.com/package/dbd.ts;DBD.TS;link;;no]`
})
```

Regular Button:
```javascript
bot.commands.add({
    type: "buttonCommand",
    code: `$if[$interactionID==click;That was a nice click!;]`
})

bot.commands.add({
    type: "basicCommand",
    name: "button",
    code: `Click The Button!
$addActionRow
$addButton[click;Click Me!;primary;;no]`
})
```

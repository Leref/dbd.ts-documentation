# $addButton

Adds a button to this action row.

### Usage

```php
$addButton[customID | link;label;style;emoji;disabled (yes/no)]
```

This function has 5 fields.

1. `customID | link` - The customID or link of this button. \| Required
2. `label` - The label that this button displays. \| Required
3. `style` - The style of this button. Can be `primary`, `secondary`, `success`, `danger`, `link`. [\(see button style previews\)](https://imgur.com/GK4HptH) \| Required
4. `emoji` - The emoji that will appear to the left of the `label`, leave empty for no emoji. \| Optional
5. `disabled` - Whether this button should be disabled or not. \| Required

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


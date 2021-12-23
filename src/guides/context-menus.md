# Context Menus
Context menus are a new, cool way to for users to interact with your bot. Context menus can be accessed by right clicking or tapping on messages/users. They're a great way to surface quick actions for your bot that target messages/users.

{% hint style="success" %}
Don't forget to add the `onInteraction` event to your main file. For example:
```javascript
bot.addEvent([
    "onMessage",
    "onInteraction"
])
```
{% endhint %}

### Creating Application Command Data
To create a context menu application, you can use the `createApplicationCommandData` method in bot class:

**Template:**
```javascript
bot.createApplicationCommandData({
    type: "type",
    name: "name"
})
```
> [View Context Menu Types](/src/typedefs/applicationcommandtypes.md)

{% hint style="warning" %}
There can be 5 guild and 5 global context menu commands per bot.
{% endhint %}

**Example:**
```javascript
bot.createApplicationCommandData({
    type: "USER",
    name: "Punch"
})
```

### Creating a Context Menu
Deploy this context menu to a guild (or globally).

**Template:**
```javascript
bot.commands.add({
    name: "deploy",
    type: "basicCommand",
    code: `$if[$botOwnerID!==$authorID;
            You can't use this command!
        ;
            $createContextMenuApplication[guildID/global;contextMenuName]
            Successfully created context menu app!
        ]`
})
```

**Example:**
```javascript
bot.commands.add({
    name: "deploy",
    type: "basicCommand",
    code: `$if[$botOwnerID!==$authorID;
            You can't use this command!
        ;
            $createContextMenuApplication[$guildID;Punch]
            Successfully created context menu app!
        ]`
})
```

### Responding to Context Menu Interactions
To respond to an interaction of a context menu, you can use the `contextMenuCommand` type.

**Template:**
```javascript
bot.commands.add({
    type: "contextMenuCommand",
    name: "name",
    code: `$reply
Hello World`
})
```

**Example:**
```javascript
bot.commands.add({
    type: "contextMenuCommand",
    name: "Punch",
    code: `$reply
        $username wants to punch <@$slashOption[user]>!`
})
```

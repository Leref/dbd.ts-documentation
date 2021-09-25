# Slash Commands
Slash Commands are the new, exciting way to build and interact with bots on Discord. With Slash Commands, all you have to do is type `/` and you're ready to use your favorite bot. Users can learn everything your bot does and easily find new features as you add them. Validation, error states, and helpful UI walks them through your commands, meaning they can get it right the first time, especially on mobile. You now have one more ally in the fight against your phone's autocorrect. Slash Commands set your users up for success instead of confusion and frustration. They separate how users think and how your code works, meaning no matter how complex your codebase and commands may get, people who love your bot will find it approachable and easy to use.


### Prerequisites
#### Scopes
Your bot must be invited with the `bot` and `applications.commands` scopes.

![](https://user-images.githubusercontent.com/69215413/134782967-44018c7e-e2f0-432c-b02d-4f99796fbc51.png)

{% hint style="warning" %}
Re-invite your bot with these scopes, else slash commands will not work.
{% endhint %}

#### onInteraction Event
Don't forget to add the `onInteraction` event to your main file. For example:
```js
bot.addEvent([
    "onMessage",
    "onInteraction"
])
```

### Limitations
- Each bot can have 100 global slash commands, as well as, 100 slash commands per guild.
- Slash commands can not share the same name.
- Slash command names can not contain special characters and must be shorter than 32 characters.

### Application Command Data
Create slash command data in your main file.

**Template:**

_With Options_
```js
bot.createApplicationCommandData({
    type: "CHAT_INPUT",
    name: "name", //Slash command name
    description: "description", //Slash command description
    options: [
        {
            name: "content", //Name of the slash command option
            description: "description", //Slash command option description
            required: true, //Whether this slash command is required
            type: "STRING" //The input type
        }
    ]
})
```

_Without Options_
```js
bot.createApplicationCommandData({
    type: "CHAT_INPUT",
    name: "slashCommandName",
    description: "slashCommandDescription"
})
```


**Example:**
```js
bot.createApplicationCommandData({
    type: "CHAT_INPUT",
    name: "say",
    description: "Repeats what you say!",
    options: [
        {
            name: "content",
            description: "What do you want me to say?",
            required: true, 
            type: "STRING"
        }
    ]
})
```

### Creating Slash Commands
Finalizing your slash commands.

{% hint style="danger" %}
`slashCommandName` must remain the same as what you inputted for the application command data.
{% endhint %}

{% hint style="info" %}
Global slash commands can take up to an hour to fully register. Guild slash commands should be registered instantly.
{% endhint %}

**Template:**
_Guild Slash Command__
```php
$createSlashCommand[guildID;slashCommandName;returnCommandID]
```

_Global Slash Command_
```php
$createSlashCommand[global;slashCommandName;returnCommandID]
```

**Examples:**
_Guild Slash Command_
```js
bot.commands.add({
    type: "basicCommand",
    name: "deploy",
    code: `$onlyIf[$botOwnerID==$authorID;]
    $createSlashCommand[$guildID;say]
    Created!`
})
```

_Global Slash Command_
```js
bot.commands.add({
    type: "basicCommand",
    name: "deploy",
    code: `$onlyIf[$botOwnerID==$authorID;]
    $createSlashCommand[global;say]
    Created!`
})
```

### Responding to Slash Commands
{% hint style="danger" %}
`slashCommandName` must remain the same as what you inputted for the application command data.
{% endhint %}

**Template:**
```js
bot.commands.add({
    type: "slashCommand",
    name: "slashCommandName",
    code: `code`
})
```

**Example:**
```js
bot.commands.add({
    type: "slashCommand",
    name: "say",
    code: `$username said: $slashOption[content]`
})
```

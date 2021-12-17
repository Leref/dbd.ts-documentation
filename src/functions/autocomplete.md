Uncomplete as autocomplete needs a new feature in order to work.
# $autocomplete
### Usage
```php
$autocomplete[name1;value1;name2;value;2...]
```

This function has two fields.

| Field | Description | Type | Required
| :--- | :--- | :--- | :---
| name | The autocomplete option name. | string | yes
| value | The value past into the next command | string | yes

{% hint style="warning" %}
`$autocomplete` can only be used in `autocompleteCommand`.
{% endhint %}

### Creating a Autcomplete Slash Command 
**Creating the Slash Command**
```javascript
bot.createApplicationCommandData({
    type: "CHAT_INPUT",
    name: "name", //Slash command name
    description: "description", //Slash command description
    options: [
        {
            name: "option", //Name of the slash command option
            description: "description", //Slash command option description
            required: true, //Whether this slash command option is required
            type: "STRING",
            autocomplete: true //YOU MUST INCLUDE THIS
        }
    ]
})
```

**Creating Autocomplete Options**\
Create a command to store the autocomplete data.

```javascript
bot.commands.add({
  type: "autocompleteCommand",
  name: "slash command name", //Replace this with your slash command name
  code: `$autocomplete[option1;option1Value;option2;option2Value;option3;option3Value]`
})

bot.commands.add({
  type: "slashCommand",
  name: "slash command name here",
  code: `$slashOption[option]` //'option' should be replaced with your autocomplete slash command option name
})

bot.createApplicationCommandData({
    type: "CHAT_INPUT",
    name: "food",
    description: "Pick a food.",
    options: [
        {
            name: "foods",
            description: "Which food do you like best?",
            required: true,
            type: "STRING",
            autocomplete: true
        }
    ]
})
```

**Autocomplete Options**\
```javascript
bot.commands.add({
  type: "autocompleteCommand",
  name: "food",
  code: `$autocomplete[Pasta;pasta;Pizza;pizza;Burger;burger]`
})
```

**Slash Command Response**
```javascript
bot.commands.add({
  type: "slashCommand",
  name: "food",
  code: `
  $if[$slashOption[foods]==pasta;
    Yum! Pasta is lovely.
  ]

  $if[$slashOption[foods]==pizza;
    Pizza is one of my favorites!
  ]

  $if[$slashOption[foods]==burger;
    Burgers are classic!
  ]
`
})
```

**Result**

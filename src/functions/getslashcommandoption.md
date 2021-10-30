---
description: Fetches data about the specified slash command's option.
---

# $getSlashCommandOption
### Usage
```php
$getSlashCommandOption[guildID | global;slash command ID;index;property]
```

| Field | Description | Type | Required 
| :---- | :---- | :---- | :----
| guildID \| global | Type of the slash command, either `global` or a guild ID. | snowflake \| string | yes
| slashCommandID | The slash command to get the option from. | snowflake | yes
| index | The index of this option. | integer | yes
| property | The data to get from this slash command option. | [SlashCommandOptionProperties](/src/typedefs/slashcommandoptionproperties.md) | yes
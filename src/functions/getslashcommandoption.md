---
description: Fetches data about the specified slash command's option.
---

# $getSlashCommandOption
### Usage
```php
$getSlashCommandOption[guildID | global;slash command ID;index;property]
```

This function has four params.

| Params | Description | Type | Required 
| :---- | :---- | :---- | :----
| guildID \| global | Type of the slash command, either `global` or a guild ID. | Snowflake \| String | Yes
| slashCommandID | The slash command to get the option from. | Snowflake | Yes
| index | The index of this option. | Integer | Yes
| property | The data to get from this slash command option. | String [(SlashCommandOptionProperties)](/src/typedefs/slashcommandoptionproperties.md) | Yes
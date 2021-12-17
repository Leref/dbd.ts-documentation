---
description: Fetches data about the specified slash command.
---

# $getSlashCommandData
### Usage
```php
$getSlashCommandData[guildID | global;slashCommandID;property]
```

This function has three params.

| Param | Description | Type | Required 
| :---- | :---- | :---- | :----
| guildID \| global | Type of the slash command, either `global` or a guild ID. | Snowflake \| String | Yes
| slashCommandID | The slash command to get the data for. | Snowflake | Yes
| [property| The data to return about the slash command. | String [(SlashCommandProperty)](/src/typedefs/slashcommandproperty.md) | Yes
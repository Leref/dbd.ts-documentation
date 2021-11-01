---
description: Fetches data about the specified slash command.
---

# $getSlashCommandData
### Usage
```php
$getSlashCommandData[guildID | global;slashCommandID;property]
```

This function has three fields.

| Field | Description | Type | Required 
| :---- | :---- | :---- | :----
| guildID \| global | Type of the slash command, either `global` or a guild ID. | snowflake \| string | yes
| slashCommandID | The slash command to get the data for. | snowflake | yes
| [property| The data to return about the slash command. | [SlashCommandProperty](/src/typedefs/slashcommandproperty.md) | yes
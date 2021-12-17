---
description: Creates a slash command.
---

# $createSlashCommand
### Usage
```php
$createSlashCommand[guildID | global;applicationCommandDataName;returnCommandID]
```
This function has three params.

| Param | Description | Type | Required
| :---- | :---- | :---- | :----
| guildID \| global | Specify global if the slash command should be global, or pass a guild ID to add the command to that guild. | Snowflake \| String | Yes
| applicationCommandDataName | The name of the slash command data to create. | String | Yes
| returnApplicationID | Whether to return the slash command ID once created. | Boolean | No

{% hint style="info" %}
See the [Slash Commands](/src/guides/slash-commands.md) article for more information.
{% endhint %}
# $createContextMenuApplication
### Usage
```php
$createSlashCommand[guildID | global;applicationCommandDataName;returnCommandID]
```
This function has three fields.

| Field | Description | Type | Required
| :---- | :---- | :---- | :----
| guildID \| global | Specify global if the slash command should be global, or pass a guild ID to add the command to that guild. | snowflake \| string | yes
| applicationCommandDataName | The name of the slash command data to create. | string | yes
| returnApplicationID | Whether to return the slash command ID once created. | boolean | no

{% hint style="info" %}
See the [Slash Commands](/src/guides/slash-commands.md) article for more information.
{% endhint %}
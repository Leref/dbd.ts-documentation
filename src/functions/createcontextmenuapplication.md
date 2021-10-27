# $createContextMenuApplication
### Usage
```php
$createContextMenuApplication[guildID | global;applicationCommandDataName;returnApplicationID]
```
This function has three fields.

| Field | Description | Type | Required
| :---- | :---- | :---- | :----
| guildID \| global | Specify global if the context menu application will be global, or pass a guild ID to add the command to that guild. | snowflake \| string | yes
| applicationCommandDataName | The name of the context menu application data to create. | string | yes
| returnApplicationID | Whether to return the context menu application ID once created. | boolean | no

{% hint style="info" %}
See the [Context Menu](/src/guides/context-menus.md) article for more information.
{% endhint %}
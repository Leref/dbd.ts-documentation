# $defer
Shows the "_Bot_ is thinking" message. This function is for commands that may take longer than 3 seconds to run. Discord throws a error if the bot doesn't respond to a interaction (e.g. slash commands) within 3 seconds of the interaction being emitted.
> This should only be used for interactions.

### Usages
#### Usage #1
```php
$defer
```
#### Usage #2
```php
$defer[ephemeral]
```
This usage has one field.
| Field  | Description | Type | Required 
| ------ | ------ | ----- | -----
| ephemeral | Whether the interaction response should be ephemeral or not. | boolean | no

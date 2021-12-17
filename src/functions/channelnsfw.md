---
description: Returns whether a channel is not-safe-for-work (NSFW).
---

# $channelNSFW
### Usage
```php
$channelNSFW[channelID]
```
This function has one param.

| Param | Description | Type | Required |
| :--- | :--- | :--- | :--- |
| channelID | The channel to return this data for. | Snowflake | Yes |

### NSFW-Only Limiter
```
$onlyIf[$channelNSFW[$channelID]==true;You need to use that command in a NSFW channel!]
```
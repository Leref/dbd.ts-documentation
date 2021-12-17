# $awaitMessage
### Usage
```php
$awaitMessage[channelID;userFilter;time;errorMessage;response1;output1;response2;output2;...etc]
```

This function has five params.

| Param | Description | Type | Required |
| :--- | :--- | :--- | :--- |
| channelID | The channel to await messages in. | Snowflake | Yes
| userFilter | List of user IDs that the bot awaits the message for (separated by commas). Use `everyone` to await any incoming message. | Snowflake \| String | Yes
| time | How long to await the user's message, before returning `errorMessage`. | Time | Yes
| errorMessage | The error to return when `time` is up, and no response has been provided. | String | No |
| output | The message response followed by the code to execute. | String | Yes

### Example
```javascript
bot.commands.add({
    type: "basicCommand",
    name: "example",
    code: `
$awaitMessage[$channelID;everyone;1m;
        $channelSendMessage[$channelID;$makeReturn[
                No one replied with a valid input.
            ]]
        ;hello;
            $channelSendMessage[$channelID;$makeReturn[
                Hello, <@$get[message_author_id]>!
            ]]
        ;uwu;
            $channelSendMessage[$channelID;$makeReturn[
                UwU, <@$get[message_author_id]>!
            ]]
        ]
`
})
```
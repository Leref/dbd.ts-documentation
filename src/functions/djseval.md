---
description: Evals discord.js code.
---

# $djsEval
### Usage
```php
$djsEval[showOutput;code]
```

This function has two fields.

| Field | Description | Type | Required |
| :--- | :--- | :--- | :--- |
| showOutput | Whether to return the output of this code. | boolean | yes
| code | The [`discord.js`](https://discord.js.org/) code to execute. | string | yes

### Examples
**Sending a Message:**
```javascript
bot.commands.add({
    type: "basicCommand",
    name: "example",
    code: `$djsEval[yes;
let result = "Hello World!"
result]` //Returns Hell
})
```
OR 
```javascript
bot.commands.add({
    type: "basicCommand",
    name: "example",
    code: `$djsEval[no;d.data.message.channel.send("Hello World")]`
})
```
**Returning the Bot's Ping:**
```javascript
bot.commands.add({
    type: "basicCommand",
    name: "example",
    code: `$djsEval[yes;
let result = d.client.ws.ping + "ms"
result]`
})
```

**Getting Info About a User:**
```javascript
bot.commands.add({
    type: "basicCommand",
    name: "example",
    code: `$djsEval[yes;const user = d.client.users.cache.get("userIDHere")
let isBot = user.bot
let userTag = user.tag
let mention = user.toString()
let creationDate = "<t:" + Math.floor(user.createdTimestamp / 1000) + ":f>"
const result = isBot + " " + userTag + " " + mention + " " + creationDate 
result]` //Returns "true/false User#000 @User date"
})
```

**Getting Info About a Message:**
```javascript
bot.commands.add({
    type: "basicCommand",
    name: "example",
    code: `$djsEval[yes;
let content = d.data.message.content
let author =  d.data.message.author.id
let creationDate = "<t:" + Math.floor(d.data.message.createdTimestamp / 1000) + ":f>"
//Your code here]`
})
```
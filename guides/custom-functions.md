# Custom Functions
DBD.TS allows you to create your own custom functions! ✨

Custom functions can be used as a way to condense and optimize codes.

#### Creating a Custom Function
**Template:**
```js
bot.createFunction({
    name: "name", //The name of this custom function
    code: `code` //The code to execute when the function is called
})
```
**Example:**
```js
bot.createFunction({
    name: "userdata",
    code: `$textSplit[$userTag&&$authorID&&$authorAvatar;&&]`
})
```

#### Using Custom Functions
Custom functions called using `$callFunction[]`.

**Example:**
```js
bot.command({
    type: "basicCommand",
    name: "example",
    code: `$callFunction[userdata]
Tag: $splitText[1]
ID: $splitText[2]
Avatar: <$splitText[3]>`
})
```

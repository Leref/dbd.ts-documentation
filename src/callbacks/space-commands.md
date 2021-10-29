# Space Commands
`spaceCommand` is a command type which makes it so the command triggers upon every message sent.\
Spaces commands don't require any other event except `onMessage`.

### Usage
```javascript
bot.commands.add({
  type: "spaceCommand",
  code: `code`
})
```

### Example
```javascript
bot.commands.add({
  type: "spaceCommand",
  code: `$setVar[messages;$sum[$getVar[messages;$authorID;member];1];$authorID;member]`
  //Requires a variable named 'messages' with type 'member'
})
```
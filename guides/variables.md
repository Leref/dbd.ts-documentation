# Variables
Variables are how we store data in DBD.TS. Data can be assigned to users, servers, etc.

### Creating a Variable
**Template:**
```js
bot.addVariable({
  name: "name",
  type: "TYPE",
  default: "defaultValue"
})
```
**Example:**
```js
bot.addVariable({
  name: "Money",
  type: "INTEGER",
  default: 0
})
```

### Variable Types
- `TEXT` - A string of characters.
- `INTEGER` - A number without decimals.
- `FLOAT` - A number with or without decimals.

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

### Setting A Variable

```
$setVar[variable;value;id;type]
```
This function has four fields.

| Field | Description | Type | Required |
| ------ | ------ | ------ | ------ |
| variableName | The name of this variable. | string | yes
| variableValue | The value this variable holds. | string | yes
| id | The ID to assign this variable to. Can be a user, server, channel, etc. | snowflake | yes
| type | The variable type, can be anything you want. You must remember it for later. | string | yes

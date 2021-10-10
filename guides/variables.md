# Variables
Variables are how we store data in DBD.TS. Variables can be assigned to users, servers, channels, etc.

### Creating a Variable
**Template:**
```js
bot.addVariable({
  name: "name", //The name of this variable
  type: "TYPE", //The variable's type
  default: "defaultValue" //The default value of this variable (if no custom value is set from setVar)
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

## Getting a Variable's Value
```
$getVar[variable;id;type]
```
This function has three fields.

| Field | Description | Type | Required |
| ------ | ------ | ------ | ------ |
| variableName | The name of the variable to get. | string | yes
| id | The ID this variable is assigned to. Can be a user, server, channel, etc. | snowflake | yes
| type | The variable's type, must match the one inputted in `$setVar[]` | string | yes

# Command Handler
### Setting Command Handler Up
{% tabs %}
{% tab title="index.js" %}
```js
bot.commands.load({
    path: "./commands/"
})
```
{% endtab %}
{% endtabs %}

{% hint style="info" %}
`commands` can be renamed to any directory folder.
{% endhint %}

`$updateCommands` will update all commands in the `./commands/` directory.

### Folder Setup
**#1:** Create a folder named `commands`.

![](https://user-images.githubusercontent.com/69215413/133940303-46d2c252-6e84-4f00-990a-0073e5807cf1.png)

**#2:** Make a subfolder.

![](https://user-images.githubusercontent.com/69215413/133940319-c4019d39-1707-433e-8914-1faca267627a.png)

**#3:** Finally, create your command file.

![](https://user-images.githubusercontent.com/69215413/133940324-c3f49bf2-1d1b-48a7-ba55-8ba6702d93d0.png)

### Example File
{% tabs %}
{% tab title="example.js" %}
```js
module.exports = {
  type: "commandType",
  name: "commandName",
  code: `code`
}
```
{% endtab %}
{% endtabs %}

Multiple Commands In One File:
{% tabs %}
{% tab title="example.js" %}
```js
module.exports = [{
  type: "commandType",
  name: "commandName",
  code: `code`
}, {
  type: "commandType",
  name: "commandName",
  code: `code`
}]
```
{% endtab %}
{% endtabs %}

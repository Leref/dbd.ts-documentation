# Statuses
### Adding a Status
{% tabs %}
{% tab title="index.js" %}
```javascript
bot.addStatus({
  name: "Some status details",
  presence: "presence", //online, idle, dnd, invisable
  type: "STATUS_TYPE", //PLAYING, WATCHING, COMPETING, or LISTENING
  duration: 12000 //Value in milliseconds. The interval between statuses (if multiple). Do not put anything below 12000 else your bot may be ratelimited.
})
```
{% endtab %}
{% endtabs %}

{% hint style="info" %}
All statuses must have a `name` property.
{% endhint %}

### Streaming Statuses
{% tabs %}
{% tab title="index.js" %}
```javascript
bot.addStatus({
  name: "Some status details",
  type: "STREAMING", //Type set to STREAMING
  url: "https://twitch.tv/some_twitch_stream" //Stream URL
})
```
{% endtab %}
{% endtabs %}

### Example Status
```javascript
bot.addStatus({
  name: "Hello World!",
  presence: "idle",
  type: "PLAYING"
})
```

![Result](https://user-images.githubusercontent.com/69215413/144689137-c491c85c-cae8-48f9-ab2c-30710907ee1b.png)
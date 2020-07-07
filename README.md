### PuddinAPI - Unofficial Documentation
`PuddinAPI is an application programming interface (api) that generates random jokes, yomomma jokes, roasts, and more.`

### Features
- Random Jokes
- Random YoMomma Jokes
- Random Roasts

### Requirements
- NPM package `snekfetch` version `4.0.4` or later.

### Tutorials
```js
const snekfetch = require("snekfetch"); // use this or node fetch

client.on('message' async (message) => {
    const { body: { joke } } = await snekfetch.get("https://puddinapi.glitch.me/api/v1/joke"); // collects the joke from the endpoint

    if (message.content === "!joke") { // creates the command for jokes
        message.channel.send(joke); // sends the joke to the channel the command was ran in
    }
});

client.on('message' async (message) => {
    const { body: { yomomma } } = await snekfetch.get("https://puddinapi.glitch.me/api/v1/yomomma"); // collects the yomomma joke from the endpoint

    if (message.content === "!yomomma") { // creates the command for yomomma jokes
        message.channel.send(yomomma); // sends the yomomma joke to the channel the command was ran in
    }
});

client.on('message' async (message) => {
    const { body: { roast } } = await snekfetch.get("https://puddinapi.glitch.me/api/v1/roast"); // collects the roast from the endpoint

    if (message.content === "!roast") { // creates the command for roasts
        message.channel.send(roast); // sends the roast to the channel the command was ran in
    }
});
```

### Credits
- PuddinArts for the creation of the API

## Task

Create web application for displaying messages. App should contain 3 tiles on the left, stack one under another, and main section as the rest. Tiles will display only the last messages received from server based on their type (1 tile = 1 type). All messages from server must be archive. In the main section create interface allowing user to browse through all messages, filter by type of message, search for specific word (with or without type filter). Use Vue 3 with Composition API, Vite, Pinia, Typescript.

## WebSocket Connection

Server will send message every 5 seconds in JSON format. Each message is an object with keys:

- `type: 'cat'|'fact'|'joke'`
- `message: string`

Create new WebSocket

```js
const ws = new WebSocket('ws://57.128.214.54:8080');
```

Add event listener for message

```js
ws.addEventListener('message', (message) => {
  console.log(`Message from server: ${JSON.parse(message.data)}`);
});
```

$background: #144746$
$class: generator-intro$

## Handling my socket

```js
const take = ec => ({ ec, type: 'TAKE' });

const createSocketChannel = (url) => eventChannel(emit => {
  const socket = io.open(url);
  socket.onMessage(emit);
});

function* generator() {
  const eventChannel = yield call(createSocketChannel, 'ws...');

  while (true) {
    const event = yield take(eventChannel);
    yield call(log, event);
  }
}
```

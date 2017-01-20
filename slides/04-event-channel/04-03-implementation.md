$background: #144746$
$class: generator-intro$

## Event Channel

```js
function eventChannel(callback) {
  let listener;

  callback((e) => {
    if (listener) {
      listener(e);
      delete listener;
    }
  });

  return cb => (listener = cb);
}
```

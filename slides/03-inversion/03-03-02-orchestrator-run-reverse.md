$background: #5e2226$
$class:inversion$

## En inversé

```js
function* inversed() {
  yield alert;
  yield alert;
}
```

```js
const generator = inversed();
let done = false

while (!done) {
  const yielded = generator.next();
  yielded.value();
  done = yielded.done;
}
```

$background: #5e2226$
$class:inversion$

## Direct Control

```js
directControl().next();
```

## Inversion of control

```js
const bob = inversed();
let done = false

while (!done) {
  const yielded = bob.next();
  yielded.value();
  done = yielded.done;
}
```

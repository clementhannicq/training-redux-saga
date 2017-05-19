$background: #5e2226$
$class:inversion$

## Retours de fonctions

```js
function* greeting() {
  const name = yield getName;
  yield () => console.log `Hello my name is ${name}`;
}
```

```js
const generator = greeting();
let done, value = false;

while (!done) {
  const yielded = generator.next(value);
  value = yielded.value();
  done = yielded.done;
}
```

note:

Assuming getName is a defined function

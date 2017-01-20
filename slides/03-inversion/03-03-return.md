$background: #5e2226$
$class:inversion$

## How do I get return values?

```js
function* unnamedGenerator4556() {
  const name = yield getName;
  yield () => console.log `Hello my name is ${name}`;
}

const generator = unnamedGenerator4556();
let done, value = false;

while (!done) {
  const yielded = generator.next(value);
  value = yielded.value();
  done = yielded.done;
}
```

note:

Assuming getName is a defined function

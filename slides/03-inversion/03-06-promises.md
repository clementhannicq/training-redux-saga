$background: #5e2226$
$class:inversion$

## What if getName was a asynchroneous?

```js
function* unnamedGenerator4557() {
  const name = yield call(getName);
  yield call(console.log, `Hello my name is ${name}`);
}

function run(generator, lastResult) {
  const { value: { fn, args }, done } = generator.next();
  if (done) { return; }
  Promise.resolve(fn(...args))
    .then(result => run(generator, result));
}

run(unnamedGenerator4557())
```

note:

Assuming getName is a defined function

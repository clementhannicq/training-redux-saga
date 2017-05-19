$background: #5e2226$
$class:inversion$

## Asynchrone

```js
function* asynchroneousGreeting() {
  const name = yield call(getNameFromApi);
  yield call(console.log, `Hello my name is ${name}`);
}
```

```js
function run(generator, lastResult) {
  const { value: { fn, args }, done } = generator.next();
  if (done) { return; }
  Promise.resolve(fn(...args))
    .then(result => run(generator, result));
}

run(asynchroneousGreeting())
```

note:

Assuming getName is a defined function

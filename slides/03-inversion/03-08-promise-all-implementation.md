$background: #5e2226$
$class:inversion$

## Promise.all!

```js
function* unnamedGenerator4557() {
  const [name, sn] = yield [ call(getName), call(getSN) ];
  yield call(console.log, `My name is ${name} ${sn}`);
}

function run(generator, lastResult) {
  const { value, done } = generator.next();
  if (done) { return; }

  if isArray(value) {
    Promise.all(value.map(call =>
      Promise.resolve(value.fn(...value.args)))
    ).then(result => run(generator, result));
  } else { /* as before */ }
}
```

note:

Assuming getName is a defined function

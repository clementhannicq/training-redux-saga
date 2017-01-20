$background: #5e2226$
$class:inversion$

## What is this? PHP?

```js
function* unnamedGenerator4557() {
  const name = yield call(getName);
  const surname = yield call(getSurname);
  yield call(console.log, `My name is ${name} ${surname}`);
}

run(unnamedGenerator4557())
```

note:

Assuming getName is a defined function

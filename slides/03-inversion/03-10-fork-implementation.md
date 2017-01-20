$background: #5e2226$
$class:inversion$

## I want this!

```js
const call = (fn, ...args) => ({ fn, args, type: 'CALL' });
const fork = (?) => ({ ?, type: 'FORK' });

function* fileExtractor() {
  yield fork(getThenPrintFile, 'bauer');
  yield fork(getThenPrintFile, 'chloe');
}
```

note:

getThenPrintFile describe a series of actions, let's use a generator

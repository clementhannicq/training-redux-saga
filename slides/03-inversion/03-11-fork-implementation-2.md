$background: #5e2226$
$class:inversion$

## I NEED this!

```js
const fork = (fn, ...args) => ({ fn, ...args, type: 'FORK' });

function* getThenPrintFile(agentId) {
  const file = yield call(getFile, agentId);
  yield call(printFile, file);
}

function* fileExtractor() {
  yield fork(getThenPrintFile, 'bauer');
  yield fork(getThenPrintFile, 'chloe');
}
```

note:

getThenPrintFile describe a series of actions, let's use a generator

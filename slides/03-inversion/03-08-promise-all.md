$background: #5e2226$
$class:inversion$

## Comme en PHP !

```js
function* printRanking() {
  const name = yield call(getNameFromApi);
  const ranking = yield call(getRankingFromApi);
  yield call(console.log, `${name}: ${ranking}`);
}
```

```js
run(printRanking())
```

note:

Assuming getName is a defined function

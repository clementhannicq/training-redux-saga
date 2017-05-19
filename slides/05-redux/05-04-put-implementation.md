$background: #3a045b$
$class: inversion$

## Du côté du middleware

```js
export default generator => store => next => action => {
  const instance = generator();

  function run(instance, lastResult) {
    // ...
    if (value.type === 'PUT') {
      store.dispatch(value.action);
      run(instance);
    }
  }

  run(instance);
}
```

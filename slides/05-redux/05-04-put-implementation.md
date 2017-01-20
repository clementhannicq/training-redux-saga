$background: #3a045b$
$class: inversion$

## On the RUN side

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

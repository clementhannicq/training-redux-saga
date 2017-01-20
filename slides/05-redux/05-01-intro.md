$background: #3a045b$
$class: inversion$

# Redux

## Is also an event channel

```js
export default generator => store => next => action => {
  const instance = generator();

  function run(instance, lastResult) {
    // ...
    if (value.type === 'TAKE' && isNotEventChannel(value.ec)) {
      if (action.type === value.ec) {
        run(instance, action)
      }
    }
  }

  run(instance);
}
```

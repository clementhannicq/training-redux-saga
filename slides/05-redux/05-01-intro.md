$background: #3a045b$
$class: inversion$

# Redux

## Nouvel helper: TAKE, pour prendre des actions

```js
export default generator => store => next => action => {
  const instance = generator();

  function run(instance, lastResult) {
    // ...
    if (value.type === 'TAKE') {
      if (action.type === value.ec) {
        run(instance, action)
      }
    }
  }

  run(instance);
}
```

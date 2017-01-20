$background: #5e2226$
$class:inversion$

## And on the run side

```js
function run(generator, lastResult) {
  const { value, done } = generator.next();
  if (done) { return; }

  if isArray(value) {
    /* as before */
  } else {
    if (value.type === 'CALL') { /* as before */ }
    if (value.type === 'FORK') {
      run(value.fn(...value.args))
      run(generator)
    }
  }
}
```

note:

Assuming getName is a defined function

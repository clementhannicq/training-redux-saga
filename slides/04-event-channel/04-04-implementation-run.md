$background: #144746$
$class: generator-intro$

## Run

```js
function run(generator, lastResult) {
  // ...

  if (value.type === 'TAKE') {
    value.ec(event => run(generator, event))
  }
}
```

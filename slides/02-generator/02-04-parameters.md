$class: generator-intro$
$background: #314566$

## Avec des parametres

```js
function* counter(initialCount) {
  let counter = initialCount;

  while (true) {
    const shouldIncrement =
      yield `Current value: ${counter}, increment?`;
    if (shouldIncrement) { initialCount ++ }
  }
}
```

note:
 - speak of while(true)

 - speak of yield to get a value from parent scope

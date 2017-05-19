$class: generator-intro$
$background: #314566$

## Execution

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

```js
const count = counter(2);

count.next().value;
// Current value: 2, increment?

count.next(true).value;
// Current value: 3, increment?

count.next(false).value;
// Current value: 3, increment?
```

note:

 - What would next().done equal to?

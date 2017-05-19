$class: generator-intro$
$background: #314566$

## Comment l'executer

```js
function* countToTwo() {
  yield `one`;
  yield `two`;
}
```

```js
const generator = countToTwo();

const returnedOne = generator.next();
// { value: 'one', done: false }

const returnedTwo = generator.next();
// { value: 'two', done: false }

const returnedThree = generator.next();
// { value: undefined, done: true }
```

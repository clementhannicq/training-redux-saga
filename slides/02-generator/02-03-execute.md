$class: generator-intro$
$background: #314566$

## How do I use it

```js
const generator = countToTwo();

const returnedOne = generator.next();
// { value: 'one', done: false }

const returnedTwo = generator.next();
// { value: 'two', done: false }

cont returnedThree = generator.next();
// { value: undefined, done: true }
```

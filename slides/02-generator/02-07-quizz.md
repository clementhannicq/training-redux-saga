$class: generator-intro$
$background: #314566$

## C'est tout cassé !

```js
  function* brokenGenerator(names) {
    const surveyResults = names.map(name => {
      const writeCode = yield `Does ${name} write code?`;
      const writeTests = yield `Does ${name} write tests?`;

      return { name, writeCode, writeTests }
    });

    yield surveyResults;
  }
```

note:

yield from lines 3 and 4 are called from a closure (= function) and not a generator!

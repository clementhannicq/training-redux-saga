$class: generator-intro$
$background: #314566$

## More complex

```js
function* bugSong(initialBugAmount) {
  let bugAmount = initialBugAmount;

  while (true) {
    const fixABug = yield `${bugAmount} bugs in my code`;
    if (fixABug) {
      bugAmount = 2*bugAmount + 8;
    }
  }
}
```

note:
 - speak of while(true)

 - speak of yield to get a value from parent scope

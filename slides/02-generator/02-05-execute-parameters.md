$class: generator-intro$
$background: #314566$

## Let's sing a song

```js
const awesomeSong = bugSong(2);

awesomeSong.next().value;
// 2 bugs in my code

awesomeSong.next(true).value;
// 12 bugs in my code

awesomeSong.next(true).value;
// 32 bugs in my code

awesomeSong.next(false).value;
// 32 bugs in my code
```

note:

 - What would next().done equal to?

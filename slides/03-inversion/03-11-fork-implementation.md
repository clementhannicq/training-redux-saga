$background: #5e2226$
$class:inversion$

## Je veux ça

```js
const call = (fn, ...args) => ({ fn, args, type: 'CALL' });
const fork = (?) => ({ ?, type: 'FORK' });

function* sendMails(users) {
  for (user in users) {
    yield fork(generateAndSendMails, user)
  }
}
```

note:

getThenPrintFile describe a series of actions, let's use a generator

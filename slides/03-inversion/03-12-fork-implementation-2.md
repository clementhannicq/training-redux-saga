$background: #5e2226$
$class:inversion$

## J'ai besoin de ça!

```js
const fork = (fn, ...args) => ({ fn, ...args, type: 'FORK' });
```

```js
function* sendMails(users) {
  for (user in users) {
    yield fork(generateAndSendMails, user)
  }
}
```

```js
function* generateAndSendMails(agentId) {
  const mail = yield call(generateMails, user);
  yield sendMail(user)
}
```

note:

getThenPrintFile describe a series of actions, let's use a generator

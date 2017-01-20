$background: #3a045b$
$class: inversion$

## Can do thunk with clean actions

```js
function* apiUsers {
  while(true) {
    const action = yield take('GET_USERS');
    const users = yield call(fetchUsers, action.filters);
  }
}
```

note:
Problem: how to save the data into the store
Dispatch an action
New helper

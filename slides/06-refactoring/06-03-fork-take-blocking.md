$background: #82adf2$

## Blocking Fork: dirty and brittle

```js
function* subSaga() {
  // ...
  yield put({ type: 'DONE' });
}


function* mainSaga() {
  yield fork(subSaga);
  yield take('DONE');
}
```

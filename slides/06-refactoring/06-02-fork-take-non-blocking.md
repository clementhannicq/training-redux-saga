$background: #82adf2$

## Non-blocking Fork

```js
function* subSaga() {
  // ...
}


function* mainSaga() {
  // ...
  yield fork(subSaga);
  // ...
}
```

$background: #82adf2$

## Reusable code: splitting sagas

This is not going to work:

```js
function* subSaga() {
  // ...
}


function* mainSaga() {
  yield call(subSaga)
}
```
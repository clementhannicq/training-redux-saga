$background: #82adf2$

## Yield*

```js
function* subSaga() {
  // ...
  return value;
}


function* mainSaga() {
  const value = yield* subSaga(params);
}
```

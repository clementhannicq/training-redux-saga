$background: #5e2226$
$class:inversion$

## En direct

```js
function* directControl() {
  alert();
  alert();
}
```

## En inversé

```js
function* inversed() {
  yield alert;
  yield alert;
}
```

$background: #5e2226$
$class:inversion$

## Direct Control

```js
function* directControl() {
  alert();
  alert();
}
```

## Inversion of control

```js
function* inversed() {
  yield alert;
  yield alert;
}
```

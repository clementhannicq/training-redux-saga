$background: #9dc17c$

## Brain dead tests

`redux-saga-test-plan`

```js
it("should get the point of sale data", () => {
  const restaurantId = "ABC";
  const token = "LKHKJHSK";

  testSaga(getPointOfSalesSaga, { restaurantId })
    .next()
    .select(getUserToken)
    .next(token)
    .call(getMenuPointsOfSales, { token })
    .next(pointOfSaleData)
    .call(getPointOfSales, { restaurantId, token })
    .next({ type: POS_TYPE.SELF })
    .put(getPointOfSalesSuccess(pointOfSaleData, POS_TYPE.SELF))
    .next()
    .isDone();
});
```
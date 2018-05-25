$background: #9dc17c$

## Better tests

`redux-saga-test-plan`

```js
it("should get the point of sale data", () => {
  const token = "LKHKJHSK";
  const restaurantId = "ABC";

  return expectSaga(getPointOfSalesSaga, { restaurantId })
    .provide([
      [select(getUserToken), token],
      [call(getMenuPointsOfSales, { token }), pointOfSaleData],
      [call(getPointOfSales, { restaurantId, token }), { type: POS_TYPE.SELF }],
      [select(getUserToken), "LKHKJHSK"],
    ])
    .put(getPointOfSalesSuccess(pointOfSaleData, POS_TYPE.SELF))
    .not.put.like({ action: { type: "ERROR_GET_POINT_OF_SALES" } })
    .run();
});
```
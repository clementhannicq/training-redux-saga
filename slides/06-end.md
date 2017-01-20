# Redux Saga

```js
function* training() {
  yield take('NATHAN_REQUESTS_TRAINING');
  const topic = yield call(findTopic);
  const slides = yield call(prepareSlides, topic);
  yield call(giveTheTraining, slides, topic);
  yield put(
    { type: 'TRAINING_DONE', topic, author: 'clementh' }
  );
  while(true) {
    const { question } = yield take('QUESTION');
    const answer = yield call(getAnswer, question);
    yield put({ type: 'ANSWER', answer });
  }
}
```

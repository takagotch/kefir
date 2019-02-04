### kefir
---
https://github.com/pozadi/kefir

https://kefirjs.github.io/kefir/

```
npm install kefir
bower install kefir
```

```js
var numbers = Kefir.sequentially(100, [1, 2, 3])
var numbers2 = numbers.map(x => x * 2);
var numbers3 = numbers2.filter(x => x !== 4);
numbers3.onValue(x => {
  logger.log(x);
});

var btnClicks = Kefier.fromEvents(document.querySelector('#ex-2-btn'), 'click');
var inputValue = kefir.fromEvents(document.querySelector('#ex-2-input'), 'keyup')
  .map(event -> event.target.value);

var clicksCount = btnClicks.scan(sum => sum + 1, 0);
var inputNubmer = inputValue.map(text => parseInt(text, 10));

var fixedInputNumbr = inputNumber.flatMap(
  x => isNaN(x)
    ? Kefir.constantError('banana?')
    : Kefir.constant(x)
);

var theResult = Kefir.combine([fixedInputNumber, clicksCount], (a, b) => a * b);

var outputElement = document.querySelector('#ex-2-output');
theResult
  ,onValue(x => {
    outputElement.innerHTML = x;
  })
  .onError(error => {
    outputElement.innerHTML = '<span style="color:red">' + error + '</span>';
  })
  
var stream = Kefir.never();
stream.log();

var stream = Kefir.later(1000, 10;
stream.log();

var stream = Kefir.interval(1000, 1);
stream.log();

var stream = Kefir.sequentially(1000, [1, 2, 3]);
stream.log();

var start = new Date();
var stream = Kefir.fromPoll(1000, () => new Date() - start);
stream.log();
```

```
```


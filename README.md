# Introduction to Asynchronous Coding in Javascript

In this chapter you will learn about some built-in functions that supports and are asynchronous code.

PS: This lession will be short

## setTimeout

- calls a function or evaluates an expression after a specified number of milliseconds
- returns the `timeout` ID
- demonstrated code is [here](https://github.com/tbhaxor/GUIDE-TO-ASYNC-CODE-IN-JS/tree/chapter-1/codes/settimeout.html)

```js
setTimeout(function() {
  // function to be executed
}, timeInMilliSeconds);
```

### Clearing Settimeout

- clears a timer set with the [`setTimeout()`](#setTimeout) method
- The **ID** value returned by `setTimeout()` is used as the parameter for the `clearTimeout()` method
- demonstrated code is [here](https://github.com/tbhaxor/GUIDE-TO-ASYNC-CODE-IN-JS/tree/chapter-1/codes/clear-settimeout.html)

```js
let obj = setTimeout(function() {
  // function to be executed
}, timeInMilliSeconds);

clearTimeout(obj);
```

## setInterval

- repeatedly calls a function, with fixed delay (_in miliseconds_)
- returns an `interval` ID
- demonstrated code is [here](https://github.com/tbhaxor/GUIDE-TO-ASYNC-CODE-IN-JS/tree/chapter-1/codes/setinterval.html)

```js
setInterval(function() {
  // function to be executed after every "timeInMilliSeconds"
}, timeInMilliSeconds);
```

### Clearing Setinterval

- clears a timer set with the [`setInterval()`](#setInterval) method
- The **ID** value returned by `setInterval()` is used as the parameter for the `clearInterval()` method
- demonstrated code is [here](https://github.com/tbhaxor/GUIDE-TO-ASYNC-CODE-IN-JS/tree/chapter-1/codes/clear-setinterval.html)

```js
let obj = setInterval(function() {
  // function to be executed after every "timeInMilliSeconds"
}, timeInMilliSeconds);

clearInterval(obj);
```

## External Resource

- [More on SetTimeout](https://developer.mozilla.org/en-US/docs/Web/API/WindowOrWorkerGlobalScope/setTimeout)
- [More on SetInterval](https://developer.mozilla.org/en-US/docs/Web/API/WindowOrWorkerGlobalScope/setInterval)

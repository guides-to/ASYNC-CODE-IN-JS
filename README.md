# Understanding and Implementing Promises

This chapter will teach about you promises in js

## What are Promises

- allows you to **associate handlers** with an asynchronous action's eventual **success value** or **failure reason**
- `then` is used to handle the _success value_ and `catch` is used to handle _failure reason_
- lets asynchronous methods return values like synchronous methods: instead of immediately returning the final value
- takes an `executor`
  - passed with the arguments `resolve` and `reject`
  - executed immediately by the _Promise_ implementation

```js
// syntax
let p = new Promise(function(resolve, reject) {
  setTimeout(function() {
    resolve("foo");
  }, 300);
});

// handling
p.then(console.log).catch(console.warn);
```

[Here](https://github.com/tbhaxor/GUIDE-TO-ASYNC-CODE-IN-JS/blob/chapter-4/codes/basic-promise.html) is the demonstration of implementation of Promises.

## Callbacks vs Promises

- easy to manage code
- neat and clean representation
- promises prevents "The Pyramid of Doom" that occurs while nesting multiple callbacks

  <p style="text-align: center"><img src="https://i.ibb.co/mS64TzT/image.png"></p>

## States of Promise

- **`pending`**: initial state, neither fulfilled nor rejected
- **`fulfilled`**: meaning that the operation completed successfully
- **`rejected`**: meaning that the operation failed

**NOTE :** Pending promise can either be _fulfilled_ with a value, or _rejected_ with a reason (error)

## Chaining Promises

- when you `return` something in first `then` block it can be handled by the following `then` block
- overcome the problem of _callbacks in callbacks_

Example: [Chaining Promise](https://github.com/tbhaxor/GUIDE-TO-ASYNC-CODE-IN-JS/blob/chapter-4/codes/chaining-promise.html)

### Handling Error in Chained Promises

You can throw an exeception in any then block, the execution will be pointed to the **first catch** block and the execution of that promise will be terminated there after

NOTE: Demonstrated [here](https://github.com/tbhaxor/GUIDE-TO-ASYNC-CODE-IN-JS/blob/chapter-4/codes/handling-error-while-chained-promises.html)

## The `fetch()` API

- an interface for fetching resources accros the internet
- provides a generic definition of [Request](https://developer.mozilla.org/en-US/docs/Web/API/Request) and [Response](https://developer.mozilla.org/en-US/docs/Web/API/Response) objects
- uses Promises
- avoiding callback hell and having to remember the complex API of XMLHttpRequest

The basics are demonstrated [here](https://github.com/tbhaxor/GUIDE-TO-ASYNC-CODE-IN-JS/blob/chapter-4/codes/fetch.html)

## Running Asynchronous lines of Code Synchronously with Promise

This can be accomplished by `async/await` keywords

### Async

"**async**" before a function means that it will returns a promise object and the return value will be wrapped in the `resolve`. The basic implementation is demonstrated [here](https://github.com/tbhaxor/GUIDE-TO-ASYNC-CODE-IN-JS/blob/chapter-4/codes/async-function.html).

Any error `throw`n in the `async` function block will be wrapped in the `reject`. The implementation of handling error in async function is demonstated [here](https://github.com/tbhaxor/GUIDE-TO-ASYNC-CODE-IN-JS/blob/chapter-4/codes/handling-error-in-async-function.html)

### Await

- works only inside async function

```js
async function worker() {
  let promise = new Promise((resolve, reject) => {
    setTimeout(() => resolve(1 + 1), 1000);
  });

  // this will wait until the promise is resolved/rejected
  // if its rejected, an exception will be thrown
  let result = await promise;

  console.log(result); // 2
}

worker();
```

The demonstration of **running async lines of code synchronously** is [here](https://github.com/tbhaxor/GUIDE-TO-ASYNC-CODE-IN-JS/blob/chapter-4/codes/async-await.html)

## External Resource

- [Resolve is not the Opposite of Reject](https://jakearchibald.com/2014/resolve-not-opposite-of-reject/)
- [IIFE](https://developer.mozilla.org/en-US/docs/Glossary/IIFE)
- [More on Fetch API](https://developer.mozilla.org/en-US/docs/Web/API/Fetch_API)
- [Sending POST Request via Fetch](https://developers.google.com/web/updates/2015/03/introduction-to-fetch#post_request)
- [Fetch Polyfill](https://github.com/github/fetch)

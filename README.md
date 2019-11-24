# Fundamentals of Asynchronous Coding

This chapter will teach about you basic theory and applications of asynchronous

## What is Asynchronous Coding

- type of parallel programming
- each unit of work runs separately from the main application thread

## Asynchronous vs Synchronous and Its Working

Since javascript is a single-threaded langauge, it doesn't support parallel execution.

In case of synchronous execution, all the code run sequentially, and in case of asynchronous programing all the (synchronous code runs at first) functions in **event-queue** are popped and executed in call stack, and then [callback](#callbacks--listeners) are called.

<p style="text-align: center"><img src="https://www.programering.com/images/remote/ZnJvbT1jbmJsb2dzJnVybD1jbWJ3NVNPeGt6UXgwaVJDRlRURUIxWXpFekx4RVROd1FUTWo5eVp0bEdic0YyTHpSV1l2eEdjMTlTYnZObUxuNVdZajkyY2xSMmJqNXlkM2QzTHZvRGMwUkhh.jpg"></p>

The **events** are building blocks of asynchronous programing in the javascrit. They can be **listened** and **fired** by the target element

The very basic implementation of events can be seen [here](https://github.com/tbhaxor/GUIDE-TO-ASYNC-CODE-IN-JS/blob/chapter-1/codes/basics-event.html).

**NOTE :** You can also send data by creating an [CustomEvent](https://developer.mozilla.org/en-US/docs/Web/API/CustomEvent), as demonstrated [here](https://github.com/tbhaxor/GUIDE-TO-ASYNC-CODE-IN-JS/blob/chapter-1/codes/data-driven-events.html)

## Callbacks / Listeners

- also called responders
- basically they are the functions that are executed when the event is fired

<p style="text-align: center"><img src="https://miro.medium.com/max/1600/1*iHhUyO4DliDwa6x_cO5E3A.gif"></p>

## Features of Asynchronous Coding

- **increase** the **performance and responsiveness** of your application
- **non blocking** io operations

## External Resource

- [Learn HTML](https://www.w3schools.com/html/default.asp)
- [Learn Javascript](https://www.w3schools.com/js/default.asp)
- [More on Events](https://developer.mozilla.org/en-US/docs/Web/API/Event)
- [Create Document Events](https://developer.mozilla.org/en-US/docs/Web/API/Document/createEvent)

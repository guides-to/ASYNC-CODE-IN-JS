# Sending Asynchronous Network Requests

In this you will learn about sending HTTP requests asynchronously via `XHR`

## What is XHR

- also called **`XMLHttpRequest`**
- in-built object to handle all http requests
- retrieve data from a URL without having to do a full page refresh
- not an _AJAX_, but used in _AJAX_

## Syntax of XHR

```js
// instancing the object
let xhr = new XMLHttpRequest();

xhr.onreadystatechange = function() {
  // body will be executed whenever "readyState" property changes
};

// Initializes a request
xhr.open("HTTP REQUEST METHOD", "RESOURCE NAME");

// actually sending the request
xhr.send("INCLUDE REQUEST BODY (IF ANY)");
```

## Example on XHR

1. [Basic XHR Application](https://github.com/tbhaxor/GUIDE-TO-ASYNC-CODE-IN-JS/blob/chapter-3/codes/basic-xhr.html)
2. [Sending POST Data with XHR](https://github.com/tbhaxor/GUIDE-TO-ASYNC-CODE-IN-JS/blob/chapter-3/codes/post-xhr.html)
3. [Sending with Custom Headers](https://github.com/tbhaxor/GUIDE-TO-ASYNC-CODE-IN-JS/blob/chapter-3/codes/sending-custom-headers.html)

## Using JQuery to Send HTT Request

- library to interact with dom
- easy to use
- methods/functions encapsulates many lines of code
- website: https://jquery.com/
- api documentation: https://api.jquery.com/

Demonstration

1. [Sending GET Request using JQuery](https://github.com/tbhaxor/GUIDE-TO-ASYNC-CODE-IN-JS/blob/chapter-3/codes/get-using-jquery.html)
2. [Sending POST Request using JQuery](https://github.com/tbhaxor/GUIDE-TO-ASYNC-CODE-IN-JS/blob/chapter-3/codes/post-using-jquery.html)

## Making XHR Synchronous

The **third** argument in `.open()` method accepts `true` or `false` to set / unset the synchronous flag. By default, it `true`

[Here](https://github.com/tbhaxor/GUIDE-TO-ASYNC-CODE-IN-JS/blob/chapter-3/codes/synchronous-xhr.html) is an example of synchronous request

## External Resource

- [XHR Properties](https://developer.mozilla.org/en-US/docs/Web/API/XMLHttpRequest#Properties)
- [XHR Response](https://www.w3schools.com/xml/ajax_xmlhttprequest_response.asp)
- [AJAX Programming](https://developer.mozilla.org/en-US/docs/Glossary/AJAX)

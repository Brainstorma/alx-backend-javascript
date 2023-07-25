# 0x01-ES6_promise

This is a project that covers the basic concepts and usage of promises in JavaScript. Promises are a way to handle asynchronous operations in a more organized and maintainable manner. This project includes several tasks where you will learn how to create, chain, and handle promises.

## Requirements

- Node.js installed
- Text editor (VS Code, Sublime, etc.)

## Installation

To get started, you need to clone the repository and navigate to the project's directory using the following commands:

```
$ git clone https://github.com/brainstorma/0x01-ES6_promise.git
$ cd 0x01-ES6_promise/
```

## Tasks

The project consists of 11 tasks which cover different aspects and concepts related to promises. Below is a brief description of each task and a link to the respective file with the solution.

### Task 0 - practice using setTimeout

In this task, you will learn how to use setTimeout to delay the execution of a function. The goal is to create a function that prints a message after a given delay.

- [0-promise.js](./0-promise.js)

### Task 1 - create a promise

In this task, you will learn how to create a simple promise. The goal is to create a function that returns a promise and resolves after a given delay.

- [1-promise.js](./1-promise.js)

### Task 2 - resolve a promise

In this task, you will learn how to resolve a promise. The goal is to create a function that returns a promise and resolves with a given value.

- [2-promise.js](./2-promise.js)

### Task 3 - reject a promise

In this task, you will learn how to reject a promise. The goal is to create a function that returns a promise and rejects with a given error message.

- [3-promise.js](./3-promise.js)

### Task 4 - handle a promise

In this task, you will learn how to handle the resolution and rejection of a promise. The goal is to create a function that returns a promise and handles the resolution and rejection with different messages.

- [4-promise.js](./4-promise.js)

### Task 5 - resolve multiple promises

In this task, you will learn how to resolve multiple promises. The goal is to create a function that returns an array of resolved promises.

- [5-promise.js](./5-promise.js)

### Task 6 - reject multiple promises

In this task, you will learn how to reject multiple promises. The goal is to create a function that returns an array of rejected promises.

- [6-promise.js](./6-promise.js)

### Task 7 - load a dictionary

In this task, you will learn how to load a dictionary from a file using promises. The goal is to create a function that reads a file and returns a promise with the parsed dictionary object.

- [7-readme.js](./7-readme.js)

### Task 8 - return promises

In this task, you will learn how to return promises. The goal is to create a function that returns a promise and resolves with a given value.

- [8-returns.js](./8-returns.js)

### Task 9 - throw an error

In this task, you will learn how to throw an error using promises. The goal is to create a function that throws an error and returns a rejected promise.

- [9-throw.js](./9-throw.js)

### Task 10 - use a finally method

In this task, you will learn how to use the finally method of promises. The goal is to create a function that logs a message in the console and returns a resolved promise.

- [100-promise.js](./100-promise.js)

## Usage

To test the solutions of each task, you can run the respective file using Node.js. For example, to test Task 0, you can run:

```
$ node 0-promise.js
```

The output will show the result of executing the function defined in the file.

## Tasks To Complete

+ [x] 0. **Keep every promise you make and only make promises you can keep**<br/>[0-promise.js](0-promise.js) contains a script that exports a function with the prototype `function getResponseFromAPI()`, which returns a Promise.

+ [x] 1. **Don't make a promise...if you know you can't keep it**<br/>[1-promise.js](1-promise.js) contains a script that exports a function with the prototype `getFullResponseFromAPI(success)`, which returns a Promise. The parameter (`success`) is a `boolean`.
  + When the argument is:
    + `true`
      + Resolve the promise by passing an object with 2 attributes:
        + `status`: `200`
        + `body`: `'Success'`
    + `false`
      + Reject the promise with an error object with the message `The fake API is not working currently`.

+ [x] 2. **Catch me if you can!**<br/>[2-then.js](2-then.js) contains a script that exports a function with the prototype `function handleResponseFromAPI(promise)`, which appends three handlers to the `promise` argument.
  + When the Promise resolves, return an object with the following attributes:
    + `status`: `200`,
    + `body`: `'success'`
  + When the Promise rejects, return an empty `Error` object.
  + For every resolution, log `Got a response from the API` to the console.

+ [x] 3. **Handle multiple successful promises**<br/>[3-all.js](3-all.js) contains a script that meets the following requirements.
  + Import `uploadPhoto` and `createUser` from [utils.js](utils.js).
  + Use the prototype below to collectively resolve all promises and log `body firstName lastName` to the console. The functions in [utils.js](utils.js) return Promises.
    ```js
    function handleProfileSignup()
    ```
  + In the event of an error, log `Signup system offline` to the console.

+ [x] 4. **Simple promise**<br/>[4-user-promise.js](4-user-promise.js) contains a script that exports a function with the prototype `function signUpUser(firstName, lastName)`, which returns a resolved promise with the object shown below.
  ```js
  {
    firstName: value,
    lastName: value,
  }
  ```

+ [x] 5. **Reject the promises**<br/>[5-photo-reject.js](5-photo-reject.js) contains a script that exports a function with the prototype `function uploadPhoto(filename)`, which returns a Promise rejecting with an Error and the string `$fileName cannot be processed`, where `fileName` is a string.

+ [x] 6. **Handle multiple promises**<br/>[6-final-user.js](6-final-user.js) contains a script that meets the following requirements.
  + Import `signUpUser` from [4-user-promise.js](4-user-promise.js) and `uploadPhoto` from [5-photo-reject.js](5-photo-reject.js).
  + Export a function named `handleProfileSignup` that accepts three arguments `firstName` (string), `lastName` (string), and `fileName` (string) and calls the two other functions (`signUpUser` and `uploadPhoto`).
  + When the promises are all settled it should return an array with the following structure:
    ```js
    [
      {
        status: status_of_the_promise,
        value: value || reason // value or error returned by the Promise
      },
      ...
    ]
    ```

+ [x] 7. **Load balancer**<br/>[7-load_balancer.js](7-load_balancer.js) contains a script that exports a function with the prototype `function loadBalancer(chinaDownload, USDownload)`, which returns the value returned by the promise that resolved the first, where `chinaDownload` and `USDownload` are Promises.

+ [x] 8. **Throw error / try catch**<br/>[8-try.js](8-try.js) contains a script that meets the following requirements.
  + Exports a function with the prototype `function divideFunction(numerator, denominator)`, where `numerator` and `denominator` are numbers.
  + When the `denominator` argument is equal to 0, the function should throw a new error with the message `cannot divide by 0`.
  + Otherwise it should return the `numerator` divided by the `denominator`.

+ [x] 9. **Throw an error**<br/>[9-try.js](9-try.js) contains a script that meets the following requirements.
  + Export a function named `guardrail` that accepts a function argument called `mathFunction`.
  + The `guardrail` function should create and return an array named `queue`.
  + When the `mathFunction` function is executed, the value returned by the function should be appended to the `queue`. If this function throws an error, the error message should be appended to the `queue`.
  + In every case, the message `Guardrail was processed` should be added to the queue.

+ [x] 10. **Await / Async**<br/>[100-await.js](100-await.js) contains a script that meets the following requirements.
  + Import `uploadPhoto` and `createUser` from [utils.js](utils.js).
  + Export an async function named `asyncUploadUser` that will call the two functions imported above and return an object with the following format:
    ```js
    {
      photo: response_from_uploadPhoto_function,
      user: response_from_createUser_function,
    }
    ```
  + Import `uploadPhoto` and `createUser` from [utils.js](utils.js).
  + If one of the async function fails, return an empty object as shown below:
    ```js
    {
      photo: null,
      user: null,
    }
    ```


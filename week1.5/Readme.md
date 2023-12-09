# Async Function, Promises and Await

### important points

- what is synchronous function?

A synchronous function is a function where the js thread is execute the code line by line. 

- what is async function

A async function is a function which allow js thread to continue execute the program preventing the thread to wait in any part of the program. 

Asynchronous function is a wrapper on another async function which js provides.

```
// my own async function
function readFileAsync (data) {
    fs.readFile('a.txt','utf-8', (err, data) => {
      if (err) {
        return error
      }
      cb(data);
    })
}

function onDone(data) {
  console.log(data);
}

readFileAsync(onDone);

```

### JS architecture

- Js architecture is divided into three section.
    - call stacks
    - web api
    - callback queue


- All the synchronous functions are put into the call stacks, making it dependent on each other.
- If the code contains some asynchronous function like ```setTimeout()``` the call back inside the setTimeout is pushed into the web api for a certain timeout (provided by user), once it completed the timeout, the function is pushed into the call back queue.

- After the JS thread finished executing the program, **Event Loop** will check for unfinished task in the call back queue, if present it will push the task into the call stack.


### Promises

promises are syntactical sugar which make asynchronous code slightly more readable

promises eventually represents the completion or failure of an asynchronous operation
ex:

```
function readFileAsync () {
  return new Promise((resolve, reject) => {
    // asynchronous operation
    fs.readFile('a.txt','utf-8', (err, data) => {
      if (err) {
        reject(err)
      } else {
        resolve(data)
      }
    })
  })  
}

function onDone(data) {
  console.log(data);
}

function onErr(err) {
  console.log("here is the error",err.code);
}

readFileAsync().then(onDone).catch(onErr)

```

**Note** In promise async function, the caller get the data from the promise to be used in the callbacks, but in callback async function the caller provides the callback and tell the js thread to execute the callback once the async function is done.

### async await
- Eliminates callbacks and .then syntax, it makes program more readable.
- await can only be called inside async function.
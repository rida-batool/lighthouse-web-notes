## Readline
The readline module in Node helps us read one line at a time. It can use any input stream e.g process.stdin.

Import the promises interface library for question function
Class: readlinePromises.Interface

1. rl.question(query[, options])
(example at the end)

The rl.question() method displays the query by writing it to the output, waits for user input to be provided on input, then invokes the callback function passing the provided input as the first argument.

When called, rl.question() will resume the input stream if it has been paused.

If the readlinePromises.Interface was created with output set to null or undefined the query is not written.

If the question is called after rl.close(), it returns a rejected promise.

2. rl.close()

The rl.close() method closes the InterfaceConstructor instance and relinquishes control over the input and output streams. When called, the 'close' event will be emitted.

Calling rl.close() does not immediately stop other events (including 'line') from being emitted by the InterfaceConstructor instance.


```javascript
const readline = require('readline');

const rl = readline.createInterface({
  input: process.stdin,
  output: process.stdout
});

rl.question('What do you think of Node.js? ', (answer) => {
  console.log(`Thank you for your valuable feedback: ${answer}`);

  rl.close();
});
```

Note: Read the important parts of the [documentation for readline](https://github.com/nodejs/node/blob/main/doc/api/readline.md).


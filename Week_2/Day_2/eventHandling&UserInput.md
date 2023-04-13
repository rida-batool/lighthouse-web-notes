## User Events
Inputs from user on interface
e.g clicking a butoon, drag and drop

### Callbacks
used to handle user events

## User Input
we want Node app to keep running while user is still enetering data

## Event Handling User Input

Let's just look at some code first:

```javascript
// on any input from stdin (standard input), output a "." to stdout
process.stdin.on('data', (key) => {
  process.stdout.write('.');
});

console.log('after callback');
```
- process.stdin takes user input
- on method takes the input and a callback function which is called each time there is user input

**The on function is a very common method name for registering callbacks to handle events.**


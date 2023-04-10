## JavaScript Functions as Objects

One of the distinctive things about JavaScript is that functions are first-class objects.

1. Functions can be stored in variables and passed around
2. Functions can do everything that other objects can do (like having properties assigned to them)

## Callback function
A callback function:

- Is a function passed (by reference) into another function (let's call that one the "receiver" function).
- The receiver function is therefore accepting behavior to perform by calling the callback function that it now has access to.
- The receiver function can decide to call the callback function at any time, as many times as it wants.

```javascript
// The second argument/parameter is expected to be a (callback) function
const findWaldo = function(names, found) {
  for (let i = 0; i < names.length; i++) {
    let name = names[i];
    if (name === "Waldo") {
      found();   // execute callback
    }
  }
}

// actionWhenFound is the callback function called in findWaldo function
const actionWhenFound = function() {
  console.log("Found him!");
}

findWaldo(["Alice", "Bob", "Waldo", "Winston"], actionWhenFound);
```
The function actionWhenFound is known as a callback function. It is first defined, then passed as an argument to another function, and finally executed once a specific event occurs.

An example using forEach():
```javascript
const findWaldo = function(names, found) {
  //forEach()
  names.forEach(function(name, index) {
    //console.log(name);
    if (name === "Waldo") {
      found(index);   // execute callback
    }
  });
};

const actionWhenFound = function(index) {
  console.log(`Found Waldo at index ${index}!`);
};

findWaldo(["Alice", "Bob", "Waldo", "Winston"], actionWhenFound);
```
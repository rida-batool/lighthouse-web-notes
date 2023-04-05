## Syntax error

```javascript
var rank = "Imperator";
var name = "Furiosa";

console.log(rank name);
```

Error message
```
node syntax-error.js
/vagrant/focal/syntax-error.js:4
console.log(rank name);
                 ^^^^
SyntaxError: Unexpected identifier
    at exports.runInThisContext (vm.js:73:16)
    at Module._compile (module.js:443:25)
    at Object.Module._extensions..js (module.js:478:10)
    at Module.load (module.js:355:32)
    at Function.Module._load (module.js:310:12)
    at Function.Module.runMain (module.js:501:10)
    at startup (node.js:129:16)
    at node.js:814:3
```

## Stack Trace
The last bit of our error message, which we ignored, was the following.

```
    at exports.runInThisContext (vm.js:73:16)
    at Module._compile (module.js:443:25)
    at Object.Module._extensions..js (module.js:478:10)
    at Module.load (module.js:355:32)
    at Function.Module._load (module.js:310:12)
    at Function.Module.runMain (module.js:501:10)
    at startup (node.js:129:16)
    at node.js:814:3
```
This bit is called a stack trace, which shows the state of our program when the error occurred.

## Unexpected Token
SyntaxError: Unexpected token errors occur when JavaScript expected something that wasn't there, which frequently means we're missing a parenthesis, bracket or curly brace. In our case, we're missing a \}.

## Reference Errors

```javascript
var firstName = "Jane";
var lastName = "Doe";

console.log(firstName, lasName); //notice lasname
```
they occur when we're trying to use the value of an undefined variable. In our case, this happened because we misspelled lastName. 

## Type Errors

```javascript
var favouriteMeal = "BREAKFAST";

console.log(favouriteMeal.toLower());
```
node type-error.js

/vagrant/focal/type-error.js:3
console.log(favouriteMeal.toLower());

                          ^

TypeError: undefined is not a function
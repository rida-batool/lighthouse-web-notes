## Every File In Node Is A Module

Every file run by Node has access to a module object.

add this to a file and run:
```javascript
console.log(module);
```
result will be:

```javascript
Module {
  id: '.',
  exports: {},
  parent: null,
  filename: '/Users/superman/codes/moduleCheck.js',
  loaded: false,
  children: [],
  paths: [ ... ] 
}
```
notice the exports: {} above. This is the object that carries the info of function to be exported.

Files usually export an object (or a function, which in JavaScript is an object anyway).

## Add this to the file importing functionfrom other file.

```javascript
const sayHelloTo = require('./myModule');
```

but without adding exporting code in our function file we will get empty {} 

so to export the function
## Add below line in the function file you want to export

```javascript
module.exports = sayHelloTo;
```

## Conclusion
We learned that in Node,

- modules are its way of organizing code into individual files
- every js file in node is implicitly a module
  * we can console.log(module) and see its details
- module.exports tells node what to export from a file
  * it defaults to {}
- we can use require with relative paths (like ./myModule)
  * it doesn't need the .js extension, as that is implied

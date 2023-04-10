## Arrow Functions

Arrow functions provide a new syntax for declaring anonymous functions, as show below.

```javascript
// BEFORE: anonymous callback as function expression 
[1,2,3].forEach(function (num) {
  console.log('num: ', num);
});

// AFTER: anonymous callback as arrow function
[1,2,3].forEach((num) => {
  console.log('num: ', num);
});
```
We can shorten it more

```javascript
[1,2,3].forEach(num => console.log('num: ', num));
```
## Caveat Regarding this

Arrow functions don't get assigned a value for this (in the way that traditional function expressions do). 

It is therefore less common to come across arrow functions which make reference to this.

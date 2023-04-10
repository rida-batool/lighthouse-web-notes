## Functions As Object Properties (AKA Methods!)


Functions that are attached to objects are often referred to as a "method". 
Other code can now invoke or call methods like these from outside the object, without having to know or care about how they run.

```javascript
const person = {
  firstName: 'Bob',
  lastName:  'Smith',
  fullName: function() {
    return this.firstName + ' ' + this.lastName;
  }
}

// Nice, now I can just say:
console.log('Hello, ' + person.fullName());
// And it's much "cleaner" every time I need their full name!
```
### Notice 'this' in example above.
 We need the method to be able to refer to the object that it is within.

 'this' refers to the object the function resides in.
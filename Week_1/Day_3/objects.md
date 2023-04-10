## Object Values
An object's values can be of any type. The following example shows an object with primitive values:

```javascript
const myObject = {
  a: 6,     // Number
  b: "abc", // String
  c: true,  // Boolean
  d: null,  // Null
};
```

When accessing an object property using the square brackets ([]) syntax, the key must be quoted (as a string). Otherwise it would be considered a variable name instead of a string literal.

```javascript
const person = { firstName: "Khurram" };
person[firstName]; 
// ReferenceError: firstName is not defined
person["firstName"]; //returns Khurram
```

If that variable name instead points to a string, then that can be an interesting way of accessing a key:

```javascript
const person = { firstName: "Khurram" };
const propertyName = "firstName";
const firstName = person[propertyName]; // interpreted as person["firstName"], and therefore works fine :)
```

### Dot notation
An alternative way to access the same value would be person.firstName.

### Square brackets
Square-bracket notation can also be used to assign new values to new or existing keys.

### Assigning a New Value to a Key

```javascript
const mary = { name: "Mary Sue" };
mary["name"] = "Mary Jane";
mary["age"]  = 22; //adding a new key:value pair
mary // shows the resulting object with both properties
```
### Objects as Values

```javascript
const person = {
  name: "Paul",
  address: {
    street: "310 W 95th",
    city: "New York",
    zipCode: 10027
  }
};
```

This demonstrates that the value associated with the address key can be another object.

```javascript
person["address"]["city"]; // => "New York"
```

### Check the type

```javascript
typeof person["phoneNumbers"];
```

```javascript
person["phoneNumbers"] instanceof Object
person["phoneNumbers"] instanceof Array
person["phoneNumbers"] instanceof String
```

### getting keys of object
Object.keys(person) //person is the object defined before

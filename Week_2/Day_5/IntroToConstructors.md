# Introduction to constructor

constructor is a special kind of method that gets executed when an object instance is created from a class.

It is like a default value for all new Objects. Every object instance created from a class with constructor, will all have same properties.

## Customizing the Constructor
Constructor method is the best way to set up default values for its object instances. Since it is a method, we can pass values to it just like other methods. 

For example, if we want to be able to specify the pizza's crust type and size when it's created, we could add the following to our class:

```javascript
class Pizza {

//contructor method with parameters to pass
  constructor(size, crust) {
    this.size = size;
    this.crust = crust;
    this.toppings = ["cheese"];
  }

  addTopping(topping) {
    this.toppings.push(topping);
  }

}
```
call the above constructor method like so:
```javascript
let pizza = new Pizza('large', 'thin');
```

## Primitives as Objects

Each primitive in JavaScript (excluding symbol which has weird rules) has a corresponding object constructor; you can see this in the following example:

```javascript
typeof(true); 
// "boolean" 
typeof(Boolean(true)); 
// => "boolean" 
typeof(new Boolean(true));
// => "object"
```

An object constructor can be invoked with the word new, as seen above.
When you use new constructor to create variable we run into problems while doing comparisons. (== , ===)

```javascript
const greeting = "Hello, world!" 
const objGreeting = new String("Hello, world!");

greeting == objGreeting; 
// => true

greeting === objGreeting; 
// => false
```
We see above that despite having the same string content, the primitive string is not the exact same as an object string. 
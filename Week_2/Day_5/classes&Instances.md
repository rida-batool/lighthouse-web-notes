## OOP Part 1
---
### Classes & Instances

1. Declare a class:

Always use Capital first letter for class name and should be a noun
```javascript
class Pizza {

}
```

2. Build Objects using a class:

```javascript
let pizza1 = new Pizza();
let pizza2 = new Pizza();
```
When you create an object using a class, it is an **instance** of that class. So pizza1 and pizza2 are instances of the Pizza class.

Above code will create two empty objects, because our class is empty.

3. Methods and Properties:

You can add a method to a class with the following syntax:
```javascript
class SomeClass {
  methodName(parameters) {
    // this is a method
  }
}
```
To add properties to a class, simply use the this keyword followed by the property name, then assign it a value:
```javascript
class SomeClass {
  someMethod() {
    this.hello = "hi"; // Created a property called hello
  }
}
```

PizzaClass continued...
```javascript
class Pizza {

  constructor() {
    this.toppings = ["cheese"];
  }

  addTopping(topping) {
    this.toppings.push(topping);
  }
}
```

The above code has two methods in the class, constructor and addToppings. 
Now we can create new objects upon this class with different toppings. 

Since a class is just a blueprint for creating objects, methods like addTopping will exist on the instances created from the class, but not on the class itself. e.g Pizza.addToppings won't work





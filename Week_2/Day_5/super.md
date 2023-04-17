## Method overriding

If you have a subclass which needs to add something extra to the method it is inheriting from its superclass. You can define that method again in subclass and call it. It will override the method in superclass. 

But that is not good solution. 

[details on topic](https://web.compass.lighthouselabs.ca/c2a7c135-03d4-4d45-84ce-16a1e2188bc6)

# Super

OOP languages allow subclasses to have a reference on the parent class. This is usually done via the super keyword, and JavaScript supports it too!

```javascript
// Super class
class Person {
  constructor(name, quirkyFact) {
    this.name = name;
    this.quirkyFact = quirkyFact;
  }

  bio() {
    return `My name is ${this.name} and here's my quirky fact: ${this.quirkyFact}`;
  }
}

class Mentor extends Person {
  // Mentor bios need to include a bit more info
  bio() {
    return `I'm a mentor at Lighthouse Labs. ${super.bio()}`;
  }
}

// DRIVER CODE

const bob = new Mentor('Bob Ross', 'I like mountains way too much');
console.log(bob.bio());

```
Using super allows us to access the superclass, plain and simple.
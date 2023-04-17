# Introduction to Inheritance

When two or more classes share the same type of state and behaviour, we can use inheritance to avoid duplication. We can create a super class which contains the mutual properties and methods that can go into new classes.

Uisng this superClass we can create more subclasses with properties specific to subclass as well plus the superclass properties. 

Example:
```javascript
// This class represents all that is common between Student and Mentor
class Person {
  // moved here b/c it was identical
  constructor(name, quirkyFact) {
    this.name = name;
    this.quirkyFact = quirkyFact;
  }

  // moved here b/c it was identical
  bio() {
    return `My name is ${this.name} and here's my quirky fact: ${this.quirkyFact}`;
  }
}
```
```javascript
class Student extends Person {
  // stays in Student class since it's specific to students only
  enroll(cohort) {
    this.cohort = cohort;
  }
}

class Mentor extends Person {
  // specific to mentors
  goOnShift() {
    this.onShift = true;
  }

  // specific to mentors
  goOffShift() {
    this.onShift = false;
  }
}
```
Student and mentor classes can inherit behaviour and state from Person class using the keyword extends. 
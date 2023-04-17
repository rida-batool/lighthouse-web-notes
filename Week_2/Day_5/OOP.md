## Terminology

```javascript
const dog = {
  sound: "woof", // Property
  breed: "shih tzu", // Property
  speak: function() { // Method
    console.log(`${this.dogBreed} says ${this.dogSound}`);
  }
};
```

An object is a little bundle of information, also known as state. Each property that an object has, can represent the state of that object. This object's sound is "woof" and its breed is "shih tzu". That is the object's state.

An object is not just state; an object also has some stuff it can do known as behaviour. This behaviour takes the form of methods, which is just the name we give to functions when they're tied to an object.

## this

The value of this is determined at the time of the call and depends on how and where it was called.

All we really need to know for OO in JavaScript, is that when you use this inside a method, this refers to the object that the method was called on.

```javascript
const dog = {
  sound: "woof",
  speak: function() {
    console.log(this.sound);
  },
  teachMeSomething: function() {
    if (dog === this) {
      console.log('dog === this');
    }
    this.speak();
  }
};

dog.teachMeSomething();
```
Whenever your method is accessing a property or another method on the same object, use this.

OO bundles (groups) together related state and logic into an object that can be passed around as a single entity.
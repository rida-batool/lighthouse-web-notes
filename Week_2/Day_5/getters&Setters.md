# Getters & Setters

It is used to access an object property. Two resons to use these?

1. Validating data before assigning it to a property
2. Computing a value on the fly instead of simply pulling it out of a property

## A better way! get and set

Since the need for getters and setters is a very common use case in OOP, Javascript classes have special get and set keywords that we can use to implement getters and setters more easily. However, in order to make this work properly, we'll have to make sure we change the property we store the size into a different name from the setter. Otherwise we'll end up in an infitite loop where the setter calls this.size which then calls the setter ...

```javascript
class Pizza {

  // ...

  // replace our custom getters / setters with these ones!
  get price() {
    const basePrice = 10;
    const toppingPrice = 2;
    return basePrice + this.toppings.length * toppingPrice;
  }

  set size(size) {
    if (size === 's' || size === 'm' || size === 'l') {
      this._size = size;
    }
  }
}
```
The only new things here are the get and set keywords in front of the getter and setter methods. The main difference we get from using these is that price and size will now be accessed as if they were value properties instead of method properties.

```javascript
let pizza = new Pizza();

pizza.price;      // instead of getPrice()
pizza.size = 's'; // instead of setSize(size)
```


Conclusion:
Setters allow us to validate data before assigning it to a property and getters allow us to compute a value on the fly instead of simply pulling it out of a property. 

[Click me to understand it more](https://web.compass.lighthouselabs.ca/days/w02d5/activities/559)

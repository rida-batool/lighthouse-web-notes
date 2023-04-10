## for...in 
we use for---in statement to iterate over objects

Example code:

```javascript
var planetMoons = {
  mercury: 0,
  venus: 0,
  earth: 1,
  mars: 2,
  jupiter: 67,
  saturn: 62,
  uranus: 27,
  neptune: 14
};
```
We can traverse over object like so:

```javascript
for (var planet in planetMoons) {
  var numberOfMoons = planetMoons[planet];
  console.log("Planet: " + planet + ", # of Moons: "+ numberOfMoons);
}
```
We have the key available to us within the scope of the loop; in the above example it is the **planet variable**. 

Notice: var numberOfMoons = planetMoons[planet];

planet is not in double quotes becaue it is a variable.

## Limitations of for ... in

 objects can sometimes have properties that they inherit from their prototype chain as well as method names. An additional filtering step is sometimes necessary:

```javascript
for (var planet in planetMoons) {
  // additional filter for object properties:
  if (planetMoons.hasOwnProperty(planet)) {
    //  ...
  }
}
```
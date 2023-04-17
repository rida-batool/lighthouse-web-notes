## Promises
 A promise represents the eventual result of an asynchronous operation. The primary way of interaction with a promise is through its **then** method, which registers callbacks to receive either a promise’s eventual value or the reason why the promise cannot be fulfilled.

- A promise is an object
- Promises do not rely on anything other than basic JavaScript
- As of ES6, JavaScript has promises supported natively in its code. In other words, they are built into the language (via Promise)

Promises allow us to turn code like this:

```javascript
// clepto.js
gotoTheirHouse(billy, () => {
  pretendToBeFriends(billy, () => {
    stealWhenNotLooking(billy.mixtapes, (items) => {
      hideInBackpack(items, () => {
        console.log("I don't feel well. I gotta go home now Billy!");
      });
    });
  });
});
```
Into this:
```javascript
// clepto_promises.js
gotoTheirHouse(billy)
  .then(pretendToBeFriends)
  .then(stealWhenNotLooking)
  .then(hideInBackpack)
  .then(() => {
    console.log("I don't feel well. I gotta go home now Billy!");
  });
  ```

  There's more to promises than just avoiding nested callbacks, such as:

- Error handling becomes much simpler with promises
- Promises make asynchronous code easier to unit test
- **Promise.all**  can be used to run multiple async operations in parallel and have a single callback to see all the results together
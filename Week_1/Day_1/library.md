### built-in console.assert

JavaScript has a built-in console.assert function.

## console.assert()

The console.assert() method writes an error message to the console if the assertion is false. If the assertion is true, nothing happens.

```javascript
const errorMsg = "the # is not even";
for (let number = 2; number <= 5; number++) {
  console.log(`the # is ${number}`);
  console.assert(number % 2 === 0, "%o", { number, errorMsg });
}
// output:
// the # is 2
// the # is 3
// Assertion failed: {number: 3, errorMsg: "the # is not even"}
// the # is 4
// the # is 5
// Assertion failed: {number: 5, errorMsg: "the # is not even"}
```

Read the [console.assert](https://developer.mozilla.org/en-US/docs/Web/API/console/assert) docs on MDN.


## Anonymous Functions
Often a callback function would not be declared or assigned to a variable, but rather would be inline like this:

```javascript
findWaldo(["Alice", "Bob", "Waldo", "Winston"], function(index) {
  console.log("Waldo is located at:", index);
});
```

We can notice here that the callback function defined "inline" here (function(result) { ... }) is not named, nor assigned to a variable. It exists only as an anonymous function, which is invoked by the function it gets passed into – in this example findWaldo.
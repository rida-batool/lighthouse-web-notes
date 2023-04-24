## Why does jQuery exist?
---

### Reason 1: Fixes Browser Compatibility issues

To get the width of the browser viewport

```
$(window).width()
```

### Reason 2: Cleaner API

The browser has built-in JavaScript functions to help you write code that interacts with the page.

You can write this bit of JavaScript to pop up an alert when the user clicks the span element

```javascript
const element = document.getElementById("foo");
element.addEventListener("click", function() {
  alert("Clicked!");
});
```

One of the nice things that jQuery does, is it wraps the native functions with a cleaner API. The code above can be replaced with the following code in jQuery:

```javascript
$("#foo").on( "click", function() {
  console.log("Foo element clicked");
});
```

It can also be written as:

```javascript
$("#foo").click(function() {
  console.log("Foo element clicked");
});
```
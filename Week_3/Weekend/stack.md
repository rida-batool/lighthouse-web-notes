## Stack
A stack often refers to the collection of technologies used in a given system.

A common stack (but by no means the most popular, given how rapidly the JS ecosystem shifts these days) is the MEAN stack, which includes Node.js, Express, but also Angular.js and MongoDB.

## ID vs Classes
We know that ids are used to identify unique elements on a page, and classes are used to identify elements of the same type.

We target elements by ID from CSS using a selector with a hashtag prefix: #buy-now-main-btn. We only expect to find 0 or 1 elements that match this selector. An element can only have one ID, but it can have many classes.

We target elements by class using a selector with a period/dot prefix: .nav-item. We expect to find 0 to n elements that match this selector, and these elements can occur anywhere.

### Use classes most of the time
Note: As a general rule, classes should be used much more frequently than IDs.

Q: So when do I use IDs, exactly?

IDs may be used when you have a unique element such as a call to action that is styled and/or behaves very differently than other elements on a page or website.

IDs also need be used when you need to reference them from the URL using the anchor hash value (also called the page fragment). Eg: http://yourdomain.com#comments will jump to the element with ID comments.

---
## Bubbling in DOM

[Event propogation and Bubbling](https://javascript.info/bubbling-and-capturing)
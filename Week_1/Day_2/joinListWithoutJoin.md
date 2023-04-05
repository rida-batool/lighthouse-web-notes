### function joinList.js

```javascript
// Test / Driver Code below...
const conceptList = ["gists", "types", "operators", "iteration", "problem solving"];
//const conceptList = [];
const concepts = function joinList(conceptList) {
  let result = "";
  for (let concept of conceptList) {
    if (result) {
      result += ", ";
    }
    result += concept;
  }
  return result;
};
//console.log(`Today I learned about ${concepts}.`);
console.log(`Today I learned about ${concepts(conceptList)}.`);
```

Above function joins an array into a comma separated string without using join function.
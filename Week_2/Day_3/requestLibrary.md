### Request package


Request is an npm package to make HTTP requests.

```javascript
const request = require('request');
request('http://www.google.com', (error, response, body) => {
  console.log('error:', error); // Print the error if one occurred
  console.log('statusCode:', response && response.statusCode); // Print the response status code if a response was received
  console.log('body:', body); // Print the HTML for the Google homepage.
});
```
Using a simple callback mechanism, this library allows us to make async requests to any http server.

---
### library to read write from file
---

[fs file library info link](https://nodejs.dev/en/learn/nodejs-file-stats/)
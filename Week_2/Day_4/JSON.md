## JSON

It stands for JavaScript Object Notation, and it's actually a subset of the JavaScript language.

JSON is built on two structures:

1. A collection of name/value pairs.
2. An ordered list of values.

An Object encoded using JSON looks like this:

```JSON
{
  "name": "New York City",
  "boroughs": [
    "Manhattan",
    "Queens",
    "Brooklyn",
    "The Bronx",
    "Staten Island"],
  "population": 8491079,
  "area_codes": [212, 347, 646, 718, 917, 929],
  "position": { "lat": 40.7127, "lng": -74.0059 }
}
```

**The JSON syntax is (and must be) valid JavaScript.**

## Serialization

The process of serialization converts objects (or data structures) into a format that can be stored or transmitted between computers (typically as a string of text). The opposite, going from String → Object is called deserialization.

Object → String (Serialization)
String → Object (Deserialization)

Two important JSON Methods:

1. JSON.parse()

* Parse a string as JSON, optionally transform the produced value and its properties, and return the value.

2. JSON.stringify()

 * Return a JSON string corresponding to the specified value, optionally including only certain properties or replacing property values in a user-defined manner.

 Example:
 ```JSON
 const jsonString = '{"a":1, "b":2, "foo":"bar"}'; // string version of a JS Object
 const obj = JSON.parse(jsonString); //returns { a: 1, b: 2, foo: 'bar' }

 //you can perform delete or update operation on obj like objects

 JSON.stringify(obj); //returns '{"a":1,"b":2,"foo":"bar"}'
 ```
## JSON Media Type
When data is sent across the web using HTTP request/responses, the Media Type for JSON data is application/json (compared to text/html for HTML). It is set via the Content-Type HTTP response header.
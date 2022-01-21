### JSON Definition

JSON stands for JavaScript Object Notation
* Is actually a subset of the JavaScript language
* Is actually language agnostic

JSON is built on two structures
* A collection of name/value pairs
* An ordered list of values

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

* Keys should always be double quoted `"strings"` 
* JSON syntax must always be valid JavaScript

### Serialization

*Serialization* converts objects into a format that can be stored or transmitted between computers

* Typically a string of text

The opposite process of going from a string to an object is called *deserialization*

#### `JSON.parse()`

 Parse a string as JSON, optionally transform the produced value and it's properites and return the value

#### `JSON.stringify()`

Return a JSON string corresponding to the specified value, optionally include only certain properties or replacing property values in a user-defined manner.

### JSON Media Type

When data is sent across the web using HTTP request/response, the Media Type for JSON data is application/json. It is sent via the Content-Type HTTP response header

### JSON for Configuration

`npm` add package.json file to project root directory. `npm` reads the file as a string and parses it into an object.
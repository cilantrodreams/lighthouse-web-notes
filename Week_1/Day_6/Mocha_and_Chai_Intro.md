### BDD

*Behavior Driven Development* is a process that emerged from test-driven development. BDD requires you to specify the behavior of your app in terms of user stories which are broken down into scenarios that can be built and tested..

### BDD Frameworks

`Mocha` is a testing framework

`Chai` is an assertion library

### Setting up

To test code in the browser

```
npm install mocha chai --save-dev
```
To test Node.js code also run

```
npm install -g mocha
```

### Testing on Node.js vs Testing in Browser

* Node doesn't require test runner file
* Node needs `require('chai)` to be set at the top of the test file
* test is run using `mocha` command in console

### Setting up Directory Structure

`test/` in project root directory with every test file placed there e.g. `test/someModuleTest.js`
* Sub directories can be used but better to start simple and change later if necessary

### Basic Test Building Block
For a testing file named `arrayTest.js`

```js
describe('Array', function() {
  it('should start empty', function() {
    // Test implementation goes here
  });

  // We can have more its here
});
```
`describe` is used to group individual test
* first parameter should indicate what's being tested
`it` is used to create the actual tests
* first parameter should provide a human-readable description of the test e.g. "it should start empty"
* test implementation is written inside the function passed into `it`

### Writing the Test Code
Example for testing if an array is empty

```js
const assert = chai.assert;

describe('Array', function() {
  it('should start empty', function() {
    var arr = [];

    assert.equal(arr.length, 0);
  });
});
```

`assert` variable is used for convenience. Assertion functions will usually take two parameters, the "actual" value (the result of the test code) and the "expected" value (what the result really should be)

### Running the Test

Run command in test folder


```
mocha arrayTest.js
```

### Test Results

Passing test will look like 

```


  Array
    ✔ should start empty


  1 passing (5ms)

```

While failing test will look like

```


  Array
    1) should start empty


  0 passing (6ms)
  1 failing

  1) Array
       should start empty:

      AssertionError: expected 1 to equal 0
      + expected - actual

      -1
      +0
      
      at Context.<anonymous> (arrayTest.js:9:12)
      at processImmediate (internal/timers.js:461:21)



```

assertion functions can optionally take a `message` parameter that is displayed when the assertion fails. e.g.

```js
assert.equal(arr.length, 0, 'Array length was not 0');
```
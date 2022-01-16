### Introduction to Modules

Every file run by Node has access to a module object

If the following line is run using node on an empty javascript file...
```js
console.log(module);
```
The output would be

```
Module {
  id: '.',
  exports: {},
  parent: null,
  filename: '/Users/superman/codes/moduleCheck.js',
  loaded: false,
  children: [],
  paths: [ ... ] 
}
```

Therefore, each file that Node runs is actually a separate module.

### Exporting Modules

A JS file must export the part that it wants to be `require`-able. Files usually export an object.

`module.exports = thingToExport;` is used to export objects and functions (which are also objects)

`const thingToImport = require(./myModule);` is used to import module into a JS file
* relative paths can be used
* above example assumes the module is in the same directory
* `.js` extension is implied and can be omitted
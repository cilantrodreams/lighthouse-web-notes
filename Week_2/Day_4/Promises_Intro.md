### Introduction

A promise represents the eventual result of an asynchronous operation. The primary way of interaction with a promise is through its then method, which registers callbacks to receive either a promise's eventual value or the reason why the promise cannot be fullfilled.

* A promise is an object that is used to wrap an asynchronous task (a callbackk) and will execute the end result of said task (fullfilled or rejected)

Chaining callbacks without promises

```js
// clepto.js
gotoTheirHouse(billy, () => {
  pretendToBeFriends(billy, () => {
    stealWhenNotLooking(billy.mixtapes, (items) => {
      hideInBackpack(items, () => {
        console.log("I don't feel well. I gotta go home now Billy!");
      });
    });
  });
});
```

Chaining callbacks with promises

```js
// clepto_promises.js
gotoTheirHouse(billy)
  .then(pretendToBeFriends)
  .then(stealWhenNotLooking)
  .then(hideInBackpack)
  .then(() => {
    console.log("I don't feel well. I gotta go home now Billy!");
  });
```
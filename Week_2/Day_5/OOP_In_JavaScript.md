### Introduction to OOP

**Object Oriented Programming** is a way of writing code that encourages modularity and reduces duplication through the use of *objects*.

It is very important to learn due to it's popularity. Many commonly used programming languages (C++, C#, Java, Python, Swift for example) are *predominantly* OO

JavaScript is not stricly OO, but ES6 has brought more OOP features that allow for it to be used in an OO way.

### Simple OOP in JavaScript

In object oriented programming, we used objects to group related variables and functions together

* An object is a bundle of information also known as a `state`
* Each property an object has can represent the state of that object
* If the property's value is a function, it's called a `method`
* `methods` are behaviors that an object can do

```js
const dog = {
  sound: "woof", // Property
  breed: "shih tzu", // Property
  speak: function() { // Method
    console.log(`${this.dogBreed} says ${this.dogSound}`);
  }
};
```

### `this`

`this` is a keyword whose value is determined when it's called and depends on how and where it was called

For OO in JavaScript, when you use `this` inside a method, `this` refers to the object that the method was called on.

```js
const dog = {
  sound: "woof",
  speak: function() {
    console.log(this.sound);
  },
  teachMeSomething: function() {
    if (dog === this) {
      console.log('dog === this');
    }
    this.speak();
  }
};

dog.teachMeSomething();
```

Whenever your method is accessing a property or another method on the *same* object, use `this`.
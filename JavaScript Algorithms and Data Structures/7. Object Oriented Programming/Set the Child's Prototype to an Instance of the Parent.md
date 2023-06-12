# Set the Child's Prototype to an Instance of the Parent

Modify the code so that instances of `Dog` inherit from `Animal`.

```js
function Animal() {}

Animal.prototype = {
  constructor: Animal,
  eat: function () {
    console.log("nom nom nom");
  },
};

function Dog() {}

// Only change code below this line

let beagle = new Dog();
```

### Solution

```js
Dog.prototype = Object.create(Animal.prototype);
let beagle = new Dog();
```

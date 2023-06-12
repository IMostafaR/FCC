# Inherit Behaviors from a Supertype

Use `Object.create` to make two instances of `Animal` named `duck` and `beagle`.

```js
function Animal() {}

Animal.prototype = {
  constructor: Animal,
  eat: function () {
    console.log("nom nom nom");
  },
};

// Only change code below this line

let duck; // Change this line
let beagle; // Change this line
```

### Solution

```js
let duck = Object.create(Animal.prototype);
let beagle = Object.create(Animal.prototype);
```

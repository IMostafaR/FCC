# Use Inheritance So You Don't Repeat Yourself

The `eat` method is repeated in both `Cat` and `Bear`. Edit the code in the spirit of DRY by moving the `eat` method to the `Animal` `supertype`.

```js
function Cat(name) {
  this.name = name;
}

Cat.prototype = {
  constructor: Cat,
  eat: function () {
    console.log("nom nom nom");
  },
};

function Bear(name) {
  this.name = name;
}

Bear.prototype = {
  constructor: Bear,
  eat: function () {
    console.log("nom nom nom");
  },
};

function Animal() {}

Animal.prototype = {
  constructor: Animal,
};
```

### Solution

```js
function Cat(name) {
  this.name = name;
}

function Bear(name) {
  this.name = name;
}

function Animal() {}

Animal.prototype = {
  constructor: Animal,
  eat: function () {
    console.log("nom nom nom");
  },
};
```

# Add Methods After Inheritance

Add all necessary code so the `Dog` object inherits from `Animal` and the `Dog`'s `prototype` constructor is set to `Dog`. Then add a `bark()` method to the `Dog` object so that `beagle` can both `eat()` and `bark()`. The `bark()` method should print `Woof!` to the console.

```js
function Animal() {}
Animal.prototype.eat = function () {
  console.log("nom nom nom");
};

function Dog() {}

// Only change code below this line

// Only change code above this line

let beagle = new Dog();
```

### Solution

```js
Dog.prototype = Object.create(Animal.prototype);
Dog.prototype.constructor = Dog;
Dog.prototype.bark = function () {
  console.log("Woof!");
};
```

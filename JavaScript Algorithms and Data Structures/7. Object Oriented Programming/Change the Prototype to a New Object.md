# Change the Prototype to a New Object

Add the property `numLegs` and the two methods `eat()` and `describe()` to the `prototype` of `Dog` by setting the `prototype` to a new object.

```js
function Dog(name) {
  this.name = name;
}

Dog.prototype = {
  // Only change code below this line
};
```

### Solution

```js
Dog.prototype = {
  numLegs: 4,
  eat() {
    console.log("nom nom nom");
  },
  describe() {
    console.log(`My dog name is ${this.name}`);
  },
};
```

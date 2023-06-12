# Understand Where an Object’s Prototype Comes From

Use `isPrototypeOf` to check the `prototype` of `beagle`.

```js
function Dog(name) {
  this.name = name;
}

let beagle = new Dog("Snoopy");

// Only change code below this line
```

### Solution

```js
Dog.prototype.isPrototypeOf(beagle);
```

# Create a Method on an Object

Using the `dog` object, give it a method called `sayLegs`. The method should return the sentence `This dog has 4 legs.`

```js
let dog = {
  name: "Spot",
  numLegs: 4,
};

dog.sayLegs();
```

### Solution

```js
let dog = {
  name: "Spot",
  numLegs: 4,
  sayLegs() {
    return `This dog has ${dog.numLegs} legs.`;
  },
};

dog.sayLegs();
```

# Make Code More Reusable with the this Keyword

Modify the `dog.sayLegs` method to remove any references to `dog`. Use the `duck` example for guidance.

```js
let dog = {
  name: "Spot",
  numLegs: 4,
  sayLegs: function () {
    return "This dog has " + dog.numLegs + " legs.";
  },
};

dog.sayLegs();
```

### Solution

```js
let dog = {
  name: "Spot",
  numLegs: 4,
  sayLegs: function () {
    return "This dog has " + this.numLegs + " legs.";
  },
};

dog.sayLegs();
```

# Understand Own Properties

Add the own properties of `canary` to the array `ownProps`.

```js
function Bird(name) {
  this.name = name;
  this.numLegs = 2;
}

let canary = new Bird("Tweety");
let ownProps = [];
// Only change code below this line
```

### Solution

```js
for (let property in canary) {
  if (canary.hasOwnProperty(property)) {
    ownProps.push(property);
  }
}
```

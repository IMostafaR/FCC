# Understand the Constructor Property

Write a `joinDogFraternity` function that takes a `candidate` parameter and, using the `constructor` property, return `true` if the candidate is a `Dog`, otherwise return `false`.

```js
function Dog(name) {
  this.name = name;
}

// Only change code below this line
function joinDogFraternity(candidate) {}
```

### Solution

```js
function joinDogFraternity(candidate) {
  return candidate.constructor === Dog ? true : false;
}
```

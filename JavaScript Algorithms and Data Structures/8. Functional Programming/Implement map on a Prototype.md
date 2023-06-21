# Implement map on a Prototype

Write your own `Array.prototype.myMap()`, which should behave exactly like `Array.prototype.map()`. You should not use the built-in `map` method. The `Array` instance can be accessed in the `myMap` method using `this`.

```js
Array.prototype.myMap = function (callback) {
  const newArray = [];
  // Only change code below this line

  // Only change code above this line
  return newArray;
};
```

### Answer

```js
Array.prototype.myMap = function (callback) {
  const newArray = [];
  for (let i = 0; i < this.length; i++) {
    newArray.push(callback(this[i], i, this));
  }
  return newArray;
};
```

or

```js
Array.prototype.myMap = function (callback) {
  const newArray = [];
  this.forEach((ele, index, arr) => newArray.push(callback(ele, index, arr)));
  return newArray;
};
```

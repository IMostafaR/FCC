# Implement the filter Method on a Prototype

Write your own `Array.prototype.myFilter()`, which should behave exactly like `Array.prototype.filter()`. You should not use the built-in `filter` method. The `Array` instance can be accessed in the `myFilter` method using `this`.

```js
Array.prototype.myFilter = function (callback) {
  const newArray = [];
  // Only change code below this line

  // Only change code above this line
  return newArray;
};
```

### Answer

```js
Array.prototype.myFilter = function (callback) {
  const newArray = [];
  for (let i = 0; i < this.length; i++) {
    if (callback(this[i], i, this)) {
      newArray.push(this[i]);
    }
  }
  return newArray;
};
```

or;

```js
Array.prototype.myFilter = function (callback) {
  const newArray = [];
  this.forEach((ele, index, array) =>
    callback(ele, index, array) ? newArray.push(ele) : null
  );
  return newArray;
};
```

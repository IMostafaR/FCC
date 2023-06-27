# Drop it

```js
function dropElements(arr, func) {
  return arr;
}

dropElements([1, 2, 3], function (n) {
  return n < 3;
});
```

### Answer

Given the array `arr`, iterate through and remove each element starting from the first element (the 0 index) until the function `func` returns `true` when the iterated element is passed through it.

Then return the rest of the array once the condition is satisfied, otherwise, `arr` should be returned as an empty array.

```js
function dropElements(arr, func) {
  for (let i = 0; i < arr.length; i++) {
    if (func(arr[i]) == false) {
      arr.shift();
      i--;
    } else {
      return arr;
    }
  }
  return arr;
}

dropElements([1, 2, 3], function (n) {
  return n < 3;
});
```

or

```js
function dropElements(arr, func) {
  const index = arr.findIndex(func);
  return index >= 0 ? arr.slice(index) : [];
}

dropElements([1, 2, 3], function (n) {
  return n < 3;
});
```

or

```js
function dropElements(arr, func) {
  while (arr.length > 0 && !func(arr[0])) {
    arr.shift();
  }
  return arr;
}

dropElements([1, 2, 3], function (n) {
  return n < 3;
});
```

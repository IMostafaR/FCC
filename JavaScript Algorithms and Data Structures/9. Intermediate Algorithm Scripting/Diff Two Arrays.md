# Diff Two Arrays

Compare two arrays and return a new array with any items only found in one of the two given arrays, but not both. In other words, return the symmetric difference of the two arrays.

**Note:** You can return the array with its elements in any order.

```js
function diffArray(arr1, arr2) {
  const newArr = [];
  return newArr;
}

diffArray([1, 2, 3, 5], [1, 2, 3, 4, 5]);
```

### Answer

```js
function diffArray(arr1, arr2) {
  const newArr = [];
  arr1.map((item) => (!arr2.includes(item) ? newArr.push(item) : null));
  arr2.map((item) => (!arr1.includes(item) ? newArr.push(item) : null));
  return newArr;
}

diffArray([1, 2, 3, 5], [1, 2, 3, 4, 5]);
```

or

```js
function diffArray(arr1, arr2) {
  let combinedArray = arr1.concat(arr2);
  let newArr = combinedArray.filter(
    (item) => !arr1.includes(item) || !arr2.includes(item)
  );
  return newArr;
}

diffArray([1, 2, 3, 5], [1, 2, 3, 4, 5]);
```

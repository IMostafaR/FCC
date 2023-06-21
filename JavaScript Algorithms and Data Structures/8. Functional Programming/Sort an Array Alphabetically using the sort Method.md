# Sort an Array Alphabetically using the sort Method

Use the `sort` method in the `alphabeticalOrder` function to sort the elements of `arr` in alphabetical order. The function should return the sorted array.

```js
function alphabeticalOrder(arr) {
  // Only change code below this line

  return arr;
  // Only change code above this line
}

alphabeticalOrder(["a", "d", "c", "a", "z", "g"]);
```

### Answer

```js
function alphabeticalOrder(arr) {
  let sortedArr = arr.sort((a, b) => (a === b ? 0 : a < b ? -1 : 1));
  return sortedArr;
}

alphabeticalOrder(["a", "d", "c", "a", "z", "g"]);
```

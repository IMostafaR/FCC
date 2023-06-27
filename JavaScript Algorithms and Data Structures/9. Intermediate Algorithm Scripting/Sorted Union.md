# Sorted Union

Write a function that takes two or more arrays and returns a new array of unique values in the order of the original provided arrays.

In other words, all values present from all arrays should be included in their original order, but with no duplicates in the final array.

The unique numbers should be sorted by their original order, but the final array should not be sorted in numerical order.

Check the assertion tests for examples.

```js
function uniteUnique(arr) {
  return arr;
}

uniteUnique([1, 3, 2], [5, 2, 1, 4], [2, 1]);
```

### Answer

```js
function uniteUnique(...arr) {
  let allNums = [];
  let uniqueArr = [];
  arr.map((smallArr) => smallArr.map((num) => allNums.push(num)));
  allNums.map((num) =>
    uniqueArr.find((uniqueNum) => uniqueNum == num) == undefined
      ? uniqueArr.push(num)
      : null
  );

  return uniqueArr;
}

uniteUnique([1, 3, 2], [5, 2, 1, 4], [2, 1]);
```

or

```js
function uniteUnique(...arr) {
  const uniqueSet = new Set(arr.flat());
  return Array.from(uniqueSet);
}

uniteUnique([1, 3, 2], [5, 2, 1, 4], [2, 1]);
```

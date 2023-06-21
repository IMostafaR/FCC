# Return a Sorted Array Without Changing the Original Array

Use the `sort` method in the `nonMutatingSort` function to sort the elements of an array in ascending order. The function should return a new array, and not mutate the `globalArray` variable.

```js
const globalArray = [5, 6, 3, 2, 9];

function nonMutatingSort(arr) {
  // Only change code below this line
  // Only change code above this line
}

nonMutatingSort(globalArray);
```

### Answer

```js
const globalArray = [5, 6, 3, 2, 9];

function nonMutatingSort(arr) {
  let newArr = [...arr];
  let sortedArr = newArr.sort((a, b) => (a === b ? 0 : a < b ? -1 : 1));
  return sortedArr;
}

nonMutatingSort(globalArray);
```

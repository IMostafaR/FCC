# Chunky Monkey

Write a function that splits an array (first argument) into groups the length of `size` (second argument) and returns them as a two-dimensional array.

```js
function chunkArrayInGroups(arr, size) {
  return arr;
}

chunkArrayInGroups(["a", "b", "c", "d"], 2);
```

### Solution

```js
function chunkArrayInGroups(arr, size) {
  let newArr = [];
  let firstIndex = 0;
  let secondIndex = size;
  for (let i = 0; i < arr.length / size; i++) {
    newArr.push(arr.slice(firstIndex, secondIndex));
    firstIndex += size;
    secondIndex += size;
  }
  return newArr;
}

chunkArrayInGroups(["a", "b", "c", "d"], 2);
```

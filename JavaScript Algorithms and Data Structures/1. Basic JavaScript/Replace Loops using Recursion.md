# Replace Loops using Recursion

Write a recursive function, `sum(arr, n)`, that returns the sum of the first `n` elements of an array `arr`.

```js
function sum(arr, n) {
  // Only change code below this line
  // Only change code above this line
}
```

### Solution

```js
function sum(arr, n) {
  if (n <= 0) {
    return 0;
  } else {
    return sum(arr, n - 1) + arr[n - 1];
  }
}
```

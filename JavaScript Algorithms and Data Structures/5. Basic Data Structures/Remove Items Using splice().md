# Remove Items Using splice()

We've initialized an array `arr`. Use `splice()` to remove elements from `arr`, so that it only contains elements that sum to the value of `10`.

```js
const arr = [2, 4, 5, 1, 7, 5, 2, 1];
// Only change code below this line

// Only change code above this line
console.log(arr);
```

### Solution

```js
const arr = [2, 4, 5, 1, 7, 5, 2, 1];
let testArr = [];
let sum;

for (let i = 0; i < arr.length; i++) {
  testArr.push(arr[i]);
  sum = testArr.reduce((total, num) => total + num, 0);

  if (sum > 10) {
    testArr.pop();
    arr.splice(i, 1);
    i--;
  }
}
console.log(arr); // [ 2, 4, 1, 2, 1 ]
```

or

```js
const arr = [2, 4, 5, 1, 7, 5, 2, 1];

let sum = 0;

for (let i = 0; i < arr.length; i++) {
  sum += arr[i];

  if (sum > 10) {
    sum -= arr[i];
    arr.splice(i, 1);
    i--;
  }
}

console.log(arr); // [ 2, 4, 1, 2, 1 ]
```

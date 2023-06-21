# Use the every Method to Check that Every Element in an Array Meets a Criteria

Use the `every` method inside the `checkPositive` function to check if every element in `arr` is positive. The function should return a Boolean value.

```js
function checkPositive(arr) {
  // Only change code below this line
  // Only change code above this line
}

checkPositive([1, 2, 3, -4, 5]);
```

### Answer

```js
function checkPositive(arr) {
  return arr.every((value) => value >= 0);
}

checkPositive([1, 2, 3, -4, 5]);
```

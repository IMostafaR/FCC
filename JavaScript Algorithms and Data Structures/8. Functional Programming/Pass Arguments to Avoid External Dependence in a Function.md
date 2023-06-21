# Pass Arguments to Avoid External Dependence in a Function

Let's update the `incrementer` function to clearly declare its dependencies.

Write the `incrementer` function so it takes an argument, and then returns a result after increasing the value by one.

```js
// The global variable
let fixedValue = 4;

// Only change code below this line
function incrementer() {
  // Only change code above this line
}
```

### Answer

```js
let fixedValue = 4;

function incrementer(value) {
  return value + 1;
}
```

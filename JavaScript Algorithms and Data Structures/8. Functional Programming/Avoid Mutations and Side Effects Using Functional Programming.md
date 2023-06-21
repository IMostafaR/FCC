# Avoid Mutations and Side Effects Using Functional Programming

Fill in the code for the function `incrementer` so it returns the value of the global variable `fixedValue` increased by one.

```js
// The global variable
let fixedValue = 4;

function incrementer() {
  // Only change code below this line
  // Only change code above this line
}
```

### Answer

```js
let fixedValue = 4;

function incrementer() {
  let newValue = fixedValue + 1;

  return newValue;
}
```

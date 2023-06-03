# Use Arrow Functions to Write Concise Anonymous Functions

Rewrite the function assigned to the variable `magic` which returns a `new Date()` to use arrow function syntax. Also, make sure nothing is defined using the keyword `var`.

```js
var magic = function () {
  return new Date();
};
```

### Solution

```js
const magic = () => new Date();
```

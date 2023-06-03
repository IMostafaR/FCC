# Mutate an Array Declared with const

An array is declared as `const s = [5, 7, 2]`. Change the array to `[2, 5, 7]` using various element assignments.

```js
const s = [5, 7, 2];
function editInPlace() {
  // Only change code below this line
  // Using s = [2, 5, 7] would be invalid
  // Only change code above this line
}
editInPlace();
```

### Solution

```js
const s = [5, 7, 2];
function editInPlace() {
  s[0] = 2;
  s[1] = 5;
  s[2] = 7;
}
editInPlace();
```

or

```js
const s = [5, 7, 2];
function editInPlace() {
  let m = [2, 5, 7];
  for (let i = 0; i < s.length; i++) {
    s[i] = m.shift();
  }
}
editInPlace();
```

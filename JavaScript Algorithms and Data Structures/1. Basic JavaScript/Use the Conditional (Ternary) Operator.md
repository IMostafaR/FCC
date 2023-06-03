# Use the Conditional (Ternary) Operator

Use the conditional operator in the `checkEqual` function to check if two numbers are equal or not. The function should return either the string `Equal` or the string `Not Equal`.

```js
function checkEqual(a, b) {}

checkEqual(1, 2);
```

### Solution

```JavaScript
function checkEqual(a, b) {
 return a == b ? "Equal" : "Not Equal";
}

checkEqual(1, 2);
```

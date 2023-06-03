# Catch Arguments Passed in the Wrong Order When Calling a Function

The function `raiseToPower` raises a base to an exponent. Unfortunately, it's not called properly - fix the code so the value of `power` is the expected 8.

```js
function raiseToPower(b, e) {
  return Math.pow(b, e);
}

let base = 2;
let exp = 3;
let power = raiseToPower(exp, base);
console.log(power); // 9
```

### Solution

```js
let power = raiseToPower(base, exp);
console.log(power); // 8
```

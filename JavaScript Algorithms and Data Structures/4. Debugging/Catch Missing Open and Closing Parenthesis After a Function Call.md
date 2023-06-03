# Catch Missing Open and Closing Parenthesis After a Function Call

Fix the code so the variable `result` is set to the value returned from calling the function `getNine`.

```js
function getNine() {
  let x = 6;
  let y = 3;
  return x + y;
}

let result = getNine;
console.log(result);

// in console
ƒ getNine() {
  var x = 6;
  var y = 3;
  return x + y;
}
```

### Solution

```js
function getNine() {
  let x = 6;
  let y = 3;
  return x + y;
}

let result = getNine();
console.log(result);
```

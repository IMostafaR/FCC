# Combine Arrays with the Spread Operator

We have defined a function `spreadOut` that returns the variable `sentence`. Modify the function using the *spread* operator so that it returns the array `['learning', 'to', 'code', 'is', 'fun']`.

```js
function spreadOut() {
  let fragment = ["to", "code"];
  let sentence; // Change this line
  return sentence;
}

console.log(spreadOut());
```

### Solution

```js
function spreadOut() {
  let fragment = ["to", "code"];
  let sentence = ["learning", ...fragment, "is", "fun"];
  return sentence;
}

console.log(spreadOut());
```

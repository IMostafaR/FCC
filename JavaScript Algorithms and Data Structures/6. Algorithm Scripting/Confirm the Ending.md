# Confirm the Ending

Check if a string (first argument, `str`) ends with the given target string (second argument, `target`).

This challenge *can* be solved with the `.endsWith()` method, which was introduced in ES2015. But for the purpose of this challenge, we would like you to use one of the JavaScript substring methods instead.

```js
function confirmEnding(str, target) {
  return str;
}

confirmEnding("Bastian", "n");
```

### Solution

```js
function confirmEnding(str, target) {
  let strEnd = "";

  for (let i = target.length; i > 0; i--) {
    strEnd += str[str.length - i];
  }
  return strEnd == target;
}

confirmEnding("Bastian", "n");
```

or

```js
function confirmEnding(str, target) {
  return str.endsWith(target);
}

confirmEnding("Bastian", "n");
```

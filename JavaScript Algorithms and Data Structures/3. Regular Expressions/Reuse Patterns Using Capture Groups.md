# Reuse Patterns Using Capture Groups

Use capture groups in `reRegex` to match a string that consists of only the same number repeated exactly three times separated by single spaces.

```js
let repeatNum = "42 42 42";
let reRegex = /change/; // Change this line
let result = reRegex.test(repeatNum);
```

### Solution

```js
let repeatNum = "42 42 42";
let reRegex = /^(\d+) \1 \1$/;
let result = reRegex.test(repeatNum);
```

# Ignore Case While Matching

Write a regex `fccRegex` to match `freeCodeCamp`, no matter its case. Your regex should not match any abbreviations or variations with spaces.

```js
let myString = "freeCodeCamp";
let fccRegex = /change/; // Change this line
let result = fccRegex.test(myString);
```

### Solution

```js
let myString = "freeCodeCamp";
let fccRegex = /FrEecOdEcAmP/i;
let result = fccRegex.test(myString);
```

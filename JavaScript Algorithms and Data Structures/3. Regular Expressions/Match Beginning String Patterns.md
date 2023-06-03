# Match Beginning String Patterns

Use the caret character in a regex to find `Cal` only in the beginning of the string `rickyAndCal`.

```js
let rickyAndCal = "Cal and Ricky both like racing.";
let calRegex = /change/; // Change this line
let result = calRegex.test(rickyAndCal);
```

### Solution

```js
let rickyAndCal = "Cal and Ricky both like racing.";
let calRegex = /^Cal/;
let result = calRegex.test(rickyAndCal);
```

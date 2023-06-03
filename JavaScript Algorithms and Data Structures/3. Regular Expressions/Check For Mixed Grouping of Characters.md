# Check For Mixed Grouping of Characters

Fix the regex so that it checks for the names of `Franklin Roosevelt` or `Eleanor Roosevelt` in a case sensitive manner and it should make concessions for middle names.

Then fix the code so that the regex that you have created is checked against `myString` and either `true` or `false` is returned depending on whether the regex matches.

```js
let myString = "Eleanor Roosevelt";
let myRegex = /False/; // Change this line
let result = false; // Change this line
// After passing the challenge experiment with myString and see how the grouping works
```

### Solution

```js
let myString = "Eleanor Roosevelt";
let myRegex = /(Franklin|Eleanor)(\s\w+.?)?\sRoosevelt/;
let result = myRegex.test(myString);
```

# Use Capture Groups to Search and Replace

Write a regex `fixRegex` using three capture groups that will search for each word in the string `one two three`. Then update the `replaceText` variable to replace `one two three` with the string `three two one` and assign the result to the `result` variable. Make sure you are utilizing capture groups in the replacement string using the dollar sign (`$`) syntax.

```js
let str = "one two three";
let fixRegex = /change/; // Change this line
let replaceText = ""; // Change this line
let result = str.replace(fixRegex, replaceText);
```

### Solution

```js
let str = "one two three";
let fixRegex = /(\w+) (\w+) (\w+)/;
let replaceText = "$3 $2 $1";
let result = str.replace(fixRegex, replaceText);
```

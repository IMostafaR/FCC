# Check for All or None

Change the regex `favRegex` to match both the American English (`favorite`) and the British English (`favourite`) version of the word.

```js
let favWord = "favorite";
let favRegex = /change/; // Change this line
let result = favRegex.test(favWord);
```

### Solution

```js
let favWord = "favorite";
let favRegex = /favou?rite/;
let result = favRegex.test(favWord);
```

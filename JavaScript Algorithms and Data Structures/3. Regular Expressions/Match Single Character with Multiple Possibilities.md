# Match Single Character with Multiple Possibilities

Use a character class with vowels (`a`, `e`, `i`, `o`, `u`) in your regex `vowelRegex` to find all the vowels in the string `quoteSample`.

**Note:** Be sure to match both upper- and lowercase vowels.

```js
let quoteSample =
  "Beware of bugs in the above code; I have only proved it correct, not tried it.";
let vowelRegex = /change/; // Change this line
let result = vowelRegex; // Change this line
```

### Solution

```js
let quoteSample =
  "Beware of bugs in the above code; I have only proved it correct, not tried it.";
let vowelRegex = /[aeiou]/gi;
let result = quoteSample.match(vowelRegex);
```

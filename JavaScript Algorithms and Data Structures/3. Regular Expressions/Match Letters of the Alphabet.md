# Match Letters of the Alphabet

Match all the letters in the string `quoteSample`.

**Note**: Be sure to match both uppercase and lowercase letters.

```js
let quoteSample = "The quick brown fox jumps over the lazy dog.";
let alphabetRegex = /change/; // Change this line
let result = alphabetRegex; // Change this line
```

### Solution

```js
let quoteSample = "The quick brown fox jumps over the lazy dog.";
let alphabetRegex = /[a-z]/gi;
let result = quoteSample.match(alphabetRegex);
```

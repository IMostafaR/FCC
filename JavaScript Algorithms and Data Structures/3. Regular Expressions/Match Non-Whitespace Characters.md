# Match Non-Whitespace Characters

Change the regex `countNonWhiteSpace` to look for multiple non-whitespace characters in a string.

```js
let sample = "Whitespace is important in separating words";
let countNonWhiteSpace = /change/; // Change this line
let result = sample.match(countNonWhiteSpace);
```

### Solution

```js
let sample = "Whitespace is important in separating words";
let countNonWhiteSpace = /\S/g;
let result = sample.match(countNonWhiteSpace);
```

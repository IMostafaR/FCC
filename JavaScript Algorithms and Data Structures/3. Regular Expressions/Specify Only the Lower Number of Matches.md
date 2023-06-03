# Specify Only the Lower Number of Matches

Change the regex `haRegex` to match the word `Hazzah` only when it has four or more letter `z`'s.

```js
let haStr = "Hazzzzah";
let haRegex = /change/; // Change this line
let result = haRegex.test(haStr);
```

```js
let haStr = "Hazzzzah";
let haRegex = /Haz{4,}ah/;
let result = haRegex.test(haStr);
```

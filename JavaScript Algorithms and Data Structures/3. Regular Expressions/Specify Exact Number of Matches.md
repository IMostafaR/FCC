# Specify Exact Number of Matches

Change the regex `timRegex` to match the word `Timber` only when it has four letter `m`'s.

```js
let timStr = "Timmmmber";
let timRegex = /change/; // Change this line
let result = timRegex.test(timStr);
```

```js
let timStr = "Timmmmber";
let timRegex = /Tim{4}ber/;
let result = timRegex.test(timStr);
```

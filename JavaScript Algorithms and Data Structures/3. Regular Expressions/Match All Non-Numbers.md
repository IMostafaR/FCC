# Match All Non-Numbers

Use the shorthand character class for non-digits `\D` to count how many non-digits are in movie titles.

```js
let movieName = "2001: A Space Odyssey";
let noNumRegex = /change/; // Change this line
let result = movieName.match(noNumRegex).length;
```

### Solution

```js
let movieName = "2001: A Space Odyssey";
let noNumRegex = /\D/g;
let result = movieName.match(noNumRegex).length;
```

# Find More Than the First Match

Using the regex `starRegex`, find and extract both `Twinkle` words from the string `twinkleStar`.

**Note**

You can have multiple flags on your regex like `/search/gi`

```js
let twinkleStar = "Twinkle, twinkle, little star";
let starRegex = /change/; // Change this line
let result = twinkleStar; // Change this line
```

### Solution

```js
let twinkleStar = "Twinkle, twinkle, little star";
let starRegex = /twinkle/gi;
let result = twinkleStar.match(starRegex);
```

# Catch Mixed Usage of Single and Double Quotes

Fix the string so it either uses different quotes for the `href` value, or escape the existing ones. Keep the double quote marks around the entire string.

```js
let innerHtml = "<p>Click here to <a href="#Home">return home</a></p>";
console.log(innerHtml);

SyntaxError: unknown: Missing semicolon. (1:43)

> 1 | let innerHtml = "<p>Click here to <a href="#Home">return home</a></p>";
    |                                            ^
  2 | console.log(innerHtml);
```

### Solution

```js
let innerHtml = '<p>Click here to <a href="#Home">return home</a></p>';
console.log(innerHtml);
```

or

```js
let innerHtml = "<p>Click here to <a href='#Home'>return home</a></p>";
console.log(innerHtml);
```

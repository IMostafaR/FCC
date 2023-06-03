# Generate Random Whole Numbers with JavaScript

Use this technique to generate and return a random whole number between `0` and `9`.

```js
function randomWholeNum() {
  return Math.random();
}
```

### Solution

```JavaScript
function randomWholeNum() {
  return Math.floor(Math.random() * 10);
}
```

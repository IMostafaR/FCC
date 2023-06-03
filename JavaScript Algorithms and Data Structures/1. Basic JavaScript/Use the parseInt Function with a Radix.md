# Use the parseInt Function with a Radix

Use `parseInt()` in the `convertToInteger` function so it converts a binary number to an integer and returns it.

```js
function convertToInteger(str) {}

convertToInteger("10011");
```

### Solution

```JavaScript
function convertToInteger(str) {
  return parseInt(str, 2)
}

convertToInteger("10011");
```

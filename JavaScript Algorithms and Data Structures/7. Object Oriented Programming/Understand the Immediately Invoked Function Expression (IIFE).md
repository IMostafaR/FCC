# Understand the Immediately Invoked Function Expression (IIFE)

Rewrite the function `makeNest` and remove its call so instead it's an anonymous immediately invoked function expression (IIFE).

```js
function makeNest() {
  console.log("A cozy nest is ready");
}

makeNest();
```

### Solution

```js
(function () {
  console.log("A cozy nest is ready");
})();
```

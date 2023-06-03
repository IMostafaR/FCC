# Boo who

Check if a value is classified as a boolean primitive. Return `true` or `false`.

Boolean primitives are `true` and `false`.

```js
function booWho(bool) {
  return bool;
}

booWho(null);
```

```js
function booWho(bool) {
  return typeof bool === "boolean";
}

booWho(null);
```

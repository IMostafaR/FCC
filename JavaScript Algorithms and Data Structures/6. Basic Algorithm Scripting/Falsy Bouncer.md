# Falsy Bouncer

Remove all falsy values from an array. Return a new array; do not mutate the original array.

Falsy values in JavaScript are `false`, `null`, `0`, `""`, `undefined`, and `NaN`.

Hint: Try converting each value to a Boolean.

```js
function bouncer(arr) {
  return arr;
}

bouncer([7, "ate", "", false, 9]);
```

### Solution

```js
function bouncer(arr) {
  return arr.filter((value) => Boolean(value));
}

bouncer([7, "ate", "", false, 9]);
```

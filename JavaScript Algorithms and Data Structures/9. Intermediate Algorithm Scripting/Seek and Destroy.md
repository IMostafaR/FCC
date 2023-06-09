# Seek and Destroy

You will be provided with an initial array (the first argument in the `destroyer` function), followed by one or more arguments. Remove all elements from the initial array that are of the same value as these arguments.

**Note:** You have to use the `arguments` object.

```js
function destroyer(arr) {
  return arr;
}

destroyer([1, 2, 3, 1, 2, 3], 2, 3);
```

### Answer

```js
function destroyer(arr, ...args) {
  arr = arr.filter((item) => !args.includes(item));
  return arr;
}

destroyer([1, 2, 3, 1, 2, 3], 2, 3);
```

or

```js
function destroyer(arr) {
  let args = Array.from(arguments);
  arr = arr.filter((item) => !args.includes(item));
  return arr;
}

destroyer([1, 2, 3, 1, 2, 3], 2, 3);
```

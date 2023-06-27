# Arguments Optional

Create a function that sums two arguments together. If only one argument is provided, then return a function that expects one argument and returns the sum.

For example, `addTogether(2, 3)` should return `5`, and `addTogether(2)` should return a function.

Calling this returned function with a single argument will then return the sum:

```js
var sumTwoAnd = addTogether(2);
```

`sumTwoAnd(3)` returns `5`.

If either argument isn't a valid number, return undefined.

```js
function addTogether() {
  return false;
}

addTogether(2, 3);
```

### Answer

```js
function addTogether(...args) {
  const [x, y] = args;

  if (args.length < 2) {
    if (typeof x !== "number") {
      return undefined;
    }
    return (y) => {
      if (typeof y !== "number") {
        return undefined;
      }
      return x + y;
    };
  }

  if (typeof x !== "number" || typeof y !== "number") {
    return undefined;
  }

  return x + y;
}

addTogether(2, 3);
```

or

```js
function addTogether(...args) {
  if (args.some((arg) => typeof arg !== "number")) {
    return undefined;
  }

  if (args.length === 2) {
    return args[0] + args[1];
  }

  if (args.length === 1) {
    const [x] = args;
    return (y) => addTogether(x, y);
  }
}

addTogether(2, 3);
```

# Steamroller

Flatten a nested array. You must account for varying levels of nesting.

Your solution should not use the `Array.prototype.flat()` or `Array.prototype.flatMap()` methods.

Global variables should not be used.

```js
function steamrollArray(arr) {
  return arr;
}

steamrollArray([1, [2], [3, [[4]]]]);
```

### Answer

```jsx
function flattenArray(el, result) {
  if (!Array.isArray(el)) {
    result.push(el);
  } else {
    for (let item of el) {
      flattenArray(item, result);
    }
  }
}

function steamrollArray(arr) {
  let flattened = [];
  for (let el of arr) {
    flattenArray(el, flattened);
  }
  return flattened;
}

steamrollArray([1, [], [3, [[4]]]]);
```

or

```js
function steamrollArray(arr) {
  return arr.reduce((result, current) => {
    if (Array.isArray(current)) {
      return result.concat(steamrollArray(current));
    }
    return result.concat(current);
  }, []);
}

steamrollArray([1, [], [3, [[4]]]]);
```

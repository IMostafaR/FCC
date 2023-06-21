# Combine Two Arrays Using the concat Method

Use the `concat` method in the `nonMutatingConcat` function to concatenate `attach` to the end of `original`. The function should return the concatenated array.

```js
function nonMutatingConcat(original, attach) {
  // Only change code below this line
  // Only change code above this line
}

const first = [1, 2, 3];
const second = [4, 5];
nonMutatingConcat(first, second);
```

### Answer

```js
function nonMutatingConcat(original, attach) {
  return original.concat(attach);
}

const first = [1, 2, 3];
const second = [4, 5];
nonMutatingConcat(first, second);
```

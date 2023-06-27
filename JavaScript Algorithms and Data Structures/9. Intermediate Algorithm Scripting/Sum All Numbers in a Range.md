# Sum All Numbers in a Range

We'll pass you an array of two numbers. Return the sum of those two numbers plus the sum of all the numbers between them. The lowest number will not always come first.

For example, `sumAll([4,1])` should return `10` because sum of all the numbers between 1 and 4 (both inclusive) is `10`.

```js
function sumAll(arr) {
  return 1;
}

sumAll([1, 4]);
```

### Answer

```js
function sumAll(arr) {
  const minNum = Math.min(...arr);
  const maxNum = Math.max(...arr);
  let sum = 0;
  for (let i = minNum; i <= maxNum; i++) {
    sum += i;
  }
  return sum;
}

sumAll([1, 4]);
```

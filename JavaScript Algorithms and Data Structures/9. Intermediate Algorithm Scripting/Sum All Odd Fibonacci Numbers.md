# Sum All Odd Fibonacci Numbers

Given a positive integer `num`, return the sum of all odd Fibonacci numbers that are less than or equal to `num`.

The first two numbers in the Fibonacci sequence are 0 and 1. Every additional number in the sequence is the sum of the two previous numbers. The first seven numbers of the Fibonacci sequence are 0, 1, 1, 2, 3, 5 and 8.

For example, `sumFibs(10)` should return `10` because all odd Fibonacci numbers less than or equal to `10` are 1, 1, 3, and 5.

```js
function sumFibs(num) {
  return num;
}

sumFibs(4);
```

### Answer

```js
function sumFibs(num) {
  let fibonacciNums = [0, 1];
  for (let i = 0; i < num - 1; i++) {
    let newNum = fibonacciNums[i] + fibonacciNums[i + 1];
    if (newNum > num) {
      break;
    }
    fibonacciNums.push(newNum);
  }
  let oddNums = fibonacciNums.filter((ele) => ele % 2 != 0);
  return oddNums.reduce((total, ele) => total + ele);
}

sumFibs(4);
```

or

```js
function sumFibs(num) {
  let prev = 0;
  let current = 1;
  let sum = 0;

  while (current <= num) {
    if (current % 2 !== 0) {
      sum += current;
    }

    const next = prev + current;
    prev = current;
    current = next;
  }

  return sum;
}
```

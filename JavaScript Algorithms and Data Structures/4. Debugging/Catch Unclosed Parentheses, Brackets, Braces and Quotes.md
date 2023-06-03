# Catch Unclosed Parentheses, Brackets, Braces and Quotes

```js
let myArray = [1, 2, 3;
let arraySum = myArray.reduce((previous, current =>  previous + current);
console.log(`Sum of array values is: ${arraySum}`);

SyntaxError: unknown: Unexpected token, expected "," (1:22)

> 1 | let myArray = [1, 2, 3;
    |                       ^
  2 | let arraySum = myArray.reduce((previous, current =>  previous + current);
  3 | console.log(`Sum of array values is: ${arraySum}`);

SyntaxError: unknown: Unexpected token, expected "," (2:72)

  1 | let myArray = [1, 2, 3];
> 2 | let arraySum = myArray.reduce((previous, current =>  previous + current);
    |                                                                         ^
  3 | console.log(`Sum of array values is: ${arraySum}`);
```

### Solution

```js
let myArray = [1, 2, 3];
let arraySum = myArray.reduce((previous, current) => previous + current);
console.log(`Sum of array values is: ${arraySum}`);
```

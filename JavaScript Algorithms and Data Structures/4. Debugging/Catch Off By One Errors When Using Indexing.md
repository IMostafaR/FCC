# Catch Off By One Errors When Using Indexing

Fix the two indexing errors in the following function so all the numbers 1 through 5 are printed to the console.

```js
function countToFive() {
  let firstFive = "12345";
  let len = firstFive.length;
  // Only change code below this line
  for (let i = 1; i <= len; i++) {
    // Only change code above this line
    console.log(firstFive[i]);
  }
}

countToFive();

// console result
2;
3;
4;
5;
undefined;
```

### Solution

```js
function countToFive() {
  let firstFive = "12345";
  let len = firstFive.length;
  for (let i = 0; i < len; i++) {
    console.log(firstFive[i]);
  }
}

countToFive();

// console result
1;
2;
3;
4;
5;
```

# Use the delete Keyword to Remove Object Properties

Use the delete keyword to remove the `oranges`, `plums`, and `strawberries` keys from the `foods` object.

```js
let foods = {
  apples: 25,
  oranges: 32,
  plums: 28,
  bananas: 13,
  grapes: 35,
  strawberries: 27,
};

// Only change code below this line

// Only change code above this line

console.log(foods);
```

### Solution

```js
let foods = {
  apples: 25,
  oranges: 32,
  plums: 28,
  bananas: 13,
  grapes: 35,
  strawberries: 27,
};

function deleteFruits(...arg) {
  for (let i = 0; i < arg.length; i++) {
    delete foods[arg[i]];
  }
}
deleteFruits("oranges", "plums", "strawberries");

console.log(foods);
```

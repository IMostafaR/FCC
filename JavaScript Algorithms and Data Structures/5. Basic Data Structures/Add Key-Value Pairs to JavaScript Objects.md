# Add Key-Value Pairs to JavaScript Objects

A `foods` object has been created with three entries. Using the syntax of your choice, add three more entries to it: `bananas` with a value of `13`, `grapes` with a value of `35`, and `strawberries` with a value of `27`.

```js
let foods = {
  apples: 25,
  oranges: 32,
  plums: 28,
};

// Only change code below this line

// Only change code above this line

console.log(foods);
```

### Solution

```jsx
let foods = {
  apples: 25,
  oranges: 32,
  plums: 28,
};

foods.bananas = 13;
foods["grapes"] = 35;
let fruit = "strawberries";
foods[fruit] = 27;

console.log(foods);
```

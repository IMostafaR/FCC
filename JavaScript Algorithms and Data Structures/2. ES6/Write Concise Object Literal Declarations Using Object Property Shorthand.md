# Write Concise Object Literal Declarations Using Object Property Shorthand

Use object property shorthand with object literals to create and return an object with `name`, `age` and `gender` properties.

```js
const createPerson = (name, age, gender) => {
  // Only change code below this line
  return {
    name: name,
    age: age,
    gender: gender,
  };
  // Only change code above this line
};
```

### Solution

```js
const createPerson = (name, age, gender) => {
  return {
    name,
    age,
    gender,
  };
};
```

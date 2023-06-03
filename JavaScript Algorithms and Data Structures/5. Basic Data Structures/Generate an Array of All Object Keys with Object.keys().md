# Generate an Array of All Object Keys with Object.keys()

Finish writing the `getArrayOfUsers` function so that it returns an array containing all the properties in the object it receives as an argument.

```js
let users = {
  Alan: {
    age: 27,
    online: false,
  },
  Jeff: {
    age: 32,
    online: true,
  },
  Sarah: {
    age: 48,
    online: false,
  },
  Ryan: {
    age: 19,
    online: true,
  },
};

function getArrayOfUsers(obj) {
  // Only change code below this line
  // Only change code above this line
}

console.log(getArrayOfUsers(users));
```

### Solution

```js
function getArrayOfUsers(obj) {
  return Object.keys(obj);
}

console.log(getArrayOfUsers(users)); // [ "Alan", "Jeff", "Sarah", "Ryan" ]
```

# Modify an Object Nested Within an Object

Here we've defined an object `userActivity`, which includes another object nested within it. Set the value of the `online` key to `45`.

```js
let userActivity = {
  id: 23894201352,
  date: "January 1, 2017",
  data: {
    totalUsers: 51,
    online: 42,
  },
};

// Only change code below this line

// Only change code above this line

console.log(userActivity);
```

### Solution

```js
let userActivity = {
  id: 23894201352,
  date: "January 1, 2017",
  data: {
    totalUsers: 51,
    online: 42,
  },
};

let { data } = userActivity;
data.online = 45;

console.log(userActivity);
```

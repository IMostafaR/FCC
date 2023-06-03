# Check if an Object has a Property

Finish writing the function so that it returns `true` if the object passed to it contains all four names, `Alan`, `Jeff`, `Sarah` and `Ryan` and returns `false` otherwise.

```js
let users = {
  Alan: {
    age: 27,
    online: true,
  },
  Jeff: {
    age: 32,
    online: true,
  },
  Sarah: {
    age: 48,
    online: true,
  },
  Ryan: {
    age: 19,
    online: true,
  },
};

function isEveryoneHere(userObj) {
  // Only change code below this line
  // Only change code above this line
}

console.log(isEveryoneHere(users));
```

### Solution

```js
function isEveryoneHere(userObj) {
  let names = ["Alan", "Jeff", "Sarah", "Ryan"];
  let counter = 0;

  for (let i = 0; i < names.length; i++) {
    if (userObj.hasOwnProperty(names[i])) {
      counter++;
    }
  }

  if (counter == names.length) {
    return true;
  } else {
    return false;
  }
}

console.log(isEveryoneHere(users));
```

or

```js
function isEveryoneHere(obj) {
  if (
    "Alan" in users &&
    "Jeff" in users &&
    "Sarah" in users &&
    "Ryan" in users
  ) {
    return true;
  } else {
    return false;
  }
}
```

or

```js
function isEveryoneHere(obj) {
  return "Alan" in users &&
    "Jeff" in users &&
    "Sarah" in users &&
    "Ryan" in users
    ? true
    : false;
}

console.log(isEveryoneHere(users));
```

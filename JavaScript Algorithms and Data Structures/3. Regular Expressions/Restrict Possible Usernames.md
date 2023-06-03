# Restrict Possible Usernames

Change the regex `userCheck` to fit the constraints listed above.

```js
let username = "JackOfAllTrades";
let userCheck = /change/; // Change this line
let result = userCheck.test(username);
```

### Solution

```js
let username = "JackOfAllTrades";
let userCheck = /^[a-z]{2,}\d*$|^[a-z]\d+\d+$/i;
let result = userCheck.test(username);
```

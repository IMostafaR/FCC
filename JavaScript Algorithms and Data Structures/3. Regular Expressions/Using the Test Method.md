# Using the Test Method

Apply the regex `myRegex` on the string `myString` using the `.test()` method.

```js
let myString = "Hello, World!";
let myRegex = /Hello/;
let result = myRegex; // Change this line
```

### Solution

```js
let result = myRegex.test(myString);
```

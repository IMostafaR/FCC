# Split a String into an Array Using the split Method

Use the `split` method inside the `splitify` function to split `str` into an array of words. The function should return the array. Note that the words are not always separated by spaces, and the array should not contain punctuation.

```js
function splitify(str) {
  // Only change code below this line
  // Only change code above this line
}

splitify("Hello World,I-am code");
```

### Answer

```js
function splitify(str) {
  let splitedArr = str.split(/\s|\W/);
  return splitedArr;
}

splitify("Hello World,I-am code");
```

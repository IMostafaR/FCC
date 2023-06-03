# Mutations

Return `true` if the string in the first element of the array contains all of the letters of the string in the second element of the array.

For example, `["hello", "Hello"]`, should return `true` because all of the letters in the second string are present in the first, ignoring case.

The arguments `["hello", "hey"]` should return `false` because the string `hello` does not contain a `y`.

Lastly, `["Alien", "line"]`, should return `true` because all of the letters in `line` are present in `Alien`.

```js
function mutation(arr) {
  return arr;
}

mutation(["hello", "hey"]);
```

### Solution

```js
function mutation(arr) {
  let newArr = arr.map((word) => word.toLowerCase());
  let bigWord = newArr[0];
  let smallWord = newArr[1];
  for (let i = 0; i < smallWord.length; i++) {
    let match = bigWord.indexOf(smallWord[i]);

    if (match == -1) {
      return false;
    }
  }
  console.log(smallWord);
  return true;
}

mutation(["hello", "hey"]);
```

# Find the Longest Word in a String

Return the length of the longest word in the provided sentence.

Your response should be a number.

```js
function findLongestWordLength(str) {
  return str.length;
}

findLongestWordLength("The quick brown fox jumped over the lazy dog");
```

### Solution

```js
function findLongestWordLength(str) {
  let strSplit = str.split(" ");
  let longestWord = 0;
  let checkLength;
  for (let i = 0; i < strArr.length; i++) {
    checkLength = strArr[i].length;
    if (longestWord < checkLength) {
      longestWord = checkLength;
    }
  }
  return longestWord;
}

findLongestWordLength("The quick brown fox jumped over the lazy dog");
```

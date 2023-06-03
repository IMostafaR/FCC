# Reverse a String

Reverse the provided string and return the reversed string.

For example, `"hello"` should become `"olleh"`.

```js
function reverseString(str) {
  return str;
}

reverseString("hello");
```

### Solution

```js
function reverseString(str) {
  let strArr = [];
  let revStrArr = [];

  for (let i = 0; i < str.length; i++) {
    strArr.push(str.slice(i, i + 1));
  }
  for (let i = 0; i < strArr.length; i++) {
    revStrArr.push(strArr[strArr.length - 1 - i]);
  }
  str = revStrArr.join("");
  return str;
}

reverseString("hello");
```

or

```js
function reverseString(str) {
  let letter;
  let revStr = "";
  for (let i = 0; i < str.length; i++) {
    letter = str.charAt(str.length - 1 - i);
    revStr += letter;
  }
  str = revStr;
  return str;
}

reverseString("hello");
```

or

```js
function reverseString(str) {
  let strArr = str.split(""); // return array
  let revStr = "";
  for (let i = strArr.length - 1; i >= 0; i--) {
    revStr += strArr[i];
  }
  str = revStr;
  return str;
}

reverseString("hello");
```

or

```js
function reverseString(str) {
  return str.split("").reverse().join("");
}
reverseString("hello");
```

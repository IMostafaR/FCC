# Repeat a String Repeat a String

Repeat a given string `str` (first argument) for `num` times (second argument). Return an empty string if `num` is not a positive number. For the purpose of this challenge, do not use the built-in `.repeat()` method.

```js
function repeatStringNumTimes(str, num) {
  return str;
}

repeatStringNumTimes("abc", 3);
```

### Solution

```js
function repeatStringNumTimes(str, num) {
  if (num >= 0) {
    let repetedStr = "";
    for (let i = 0; i < num; i++) {
      repetedStr += str;
    }
    return repetedStr;
  } else {
    return "";
  }
}

repeatStringNumTimes("abc", 3);
```

or

```js
function repeatStringNumTimes(string, times) {
  if (times < 0) return "";
  if (times === 1) return string;
  else return string + repeatStringNumTimes(string, times - 1);
}
repeatStringNumTimes("abc", 3);
```

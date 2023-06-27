# Missing letters

Find the missing letter in the passed letter range and return it.

If all letters are present in the range, return `undefined`.

```js
function fearNotLetter(str) {
  return str;
}

fearNotLetter("abce");
```

### Answers

```js
function fearNotLetter(str) {
  let unicode = str.charCodeAt(0);
  for (let i = 0; i < str.length; i++) {
    if (str.charCodeAt(i) != unicode) {
      return String.fromCharCode(unicode);
    }
    unicode++;
  }
  return undefined;
}

fearNotLetter("abce");
```

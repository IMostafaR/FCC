# **Caesars Cipher**

One of the simplest and most widely known *ciphers* is a *Caesar cipher*, also known as a *shift cipher*. In a shift cipher the meanings of the letters are shifted by some set amount.

A common modern use is the [ROT13](https://www.freecodecamp.org/news/how-to-code-the-caesar-cipher-an-introduction-to-basic-encryption-3bf77b4e19f7/) cipher, where the values of the letters are shifted by 13 places. Thus `A ↔ N`, `B ↔ O` and so on.

Write a function which takes a [ROT13](https://www.freecodecamp.org/news/how-to-code-the-caesar-cipher-an-introduction-to-basic-encryption-3bf77b4e19f7/) encoded string as input and returns a decoded string.

All letters will be uppercase. Do not transform any non-alphabetic character (i.e. spaces, punctuation), but do pass them on.

```js
function rot13(str) {
  return str;
}

rot13("SERR PBQR PNZC");
```

### Answer

```js
function rot13(str) {
  const charToDecimal = (char) =>
    /[A-Z]/.test(char) ? char.charCodeAt(0) : char;

  const shiftChar = (decimal) => {
    if (typeof decimal !== "number") {
      return decimal;
    }
    if (decimal - 13 >= 65) {
      return decimal - 13;
    } else {
      return decimal - 13 + 26;
    }
  };

  const decodedStr = str
    .split("")
    .map((char) => shiftChar(charToDecimal(char)))
    .map((dec) => (typeof dec === "number" ? String.fromCharCode(dec) : dec))
    .join("");

  console.log(decodedStr);
  return decodedStr;
}

rot13("SERR PBQR PNZC");
```

# Convert HTML Entities

Convert the characters `&`, `<`, `>`, `"` (double quote), and `'` (apostrophe), in a string to their corresponding HTML entities.

```js
function convertHTML(str) {
  return str;
}

convertHTML("Dolce & Gabbana");
```

### Answer

```js
function convertHTML(str) {
  let entities = {
    "&": "&amp;",
    "<": "&lt;",
    ">": "&gt;",
    '"': "&quot;",
    "'": "&apos;",
  };
  let strArr = str.split("");
  strArr.map((ele, i) =>
    entities.hasOwnProperty(ele) ? (strArr[i] = entities[ele]) : null
  );
  return strArr.join("");
}

convertHTML("Dolce & Gabbana");
```

or

```js
function convertHTML(str) {
  return str
    .replace(/&/g, "&amp;")
    .replace(/</g, "&lt;")
    .replace(/>/g, "&gt;")
    .replace(/"/g, "&quot;")
    .replace(/'/g, "&apos;");
}

convertHTML("Dolce & Gabbana");
```

or

```js
function convertHTML(str) {
  const entities = {
    "&": "&amp;",
    "<": "&lt;",
    ">": "&gt;",
    '"': "&quot;",
    "'": "&apos;",
  };

  return str.replace(/([&<>"'])/g, (match) => entities[match]);
}

convertHTML("Dolce & Gabbana");
```

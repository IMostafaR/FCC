# Use export to Share a Code Block

There are two string-related functions in the editor. Export both of them using the method of your choice.

```js
const uppercaseString = (string) => {
  return string.toUpperCase();
};

const lowercaseString = (string) => {
  return string.toLowerCase();
};
```

### Solution

```js
export { uppercaseString, lowercaseString };
```

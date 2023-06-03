# Catch Misspelled Variable and Function Names

Fix the two spelling errors in the code so the `netWorkingCapital` calculation works.

```jsx
let receivables = 10;
let payables = 8;
let netWorkingCapital = recievables - payable;
console.log(`Net working capital is: ${netWorkingCapital}`);

// ReferenceError: recievables is not defined
// ReferenceError: payable is not defined
```

### Solution

```js
let receivables = 10;
let payables = 8;
let netWorkingCapital = receivables - payables;
console.log(`Net working capital is: ${netWorkingCapital}`);
```

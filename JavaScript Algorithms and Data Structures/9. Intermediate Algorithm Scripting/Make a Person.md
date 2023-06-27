# Make a Person

Fill in the object constructor with the following methods below:

```js
getFirstName();
getLastName();
getFullName();
setFirstName(first);
setLastName(last);
setFullName(firstAndLast);
```

Run the tests to see the expected output for each method. The methods that take an argument must accept only one argument and it has to be a string. These methods must be the only available means of interacting with the object.

```js
const Person = function (firstAndLast) {
  this.getFullName = function () {
    return "";
  };
  return firstAndLast;
};

const bob = new Person("Bob Ross");
bob.getFullName();
```

### Answer

```js
const Person = function (firstAndLast) {
  let [firstName, lastName] = firstAndLast.split(" ");

  this.getFirstName = () => firstName;
  this.getLastName = () => lastName;
  this.getFullName = () => `${this.getFirstName()} ${this.getLastName()}`;
  this.setFirstName = (first) => (firstName = first);
  this.setLastName = (last) => (lastName = last);
  this.setFullName = (firstAndLast) => {
    [firstName, lastName] = firstAndLast.split(" ");
    return `${firstName} ${lastName}`;
  };
};

const bob = new Person("Bob Ross");
bob.getFullName();
```

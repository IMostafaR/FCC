# Use a Mixin to Add Common Behavior Between Unrelated Objects

Create a mixin named `glideMixin` that defines a method named `glide`. Then use the `glideMixin` to give both `bird` and `boat` the ability to glide.

```js
let bird = {
  name: "Donald",
  numLegs: 2,
};

let boat = {
  name: "Warrior",
  type: "race-boat",
};

// Only change code below this line
```

### Solution

```js
let glideMixin = function (obj) {
  obj.glide = function () {
    console.log("Gliding");
  };
};

glideMixin(bird);
glideMixin(boat);
```

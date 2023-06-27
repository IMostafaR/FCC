# Pig Latin

Translate the provided string to Pig Latin. Input strings are guaranteed to be English words in all lowercase.

```js
function translatePigLatin(str) {
  return str;
}

translatePigLatin("consonant");
```

### Answer

```js
function translatePigLatin(str) {
  let regex = /^[^aeiou]+/g;
  let consonants = str.match(regex);
  if (consonants == null) {
    str = str.concat("way");
  } else {
    str = str.replace(consonants, "").concat(consonants).concat("ay");
  }
  return str;
}

translatePigLatin("consonant");
```

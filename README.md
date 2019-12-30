# js-cheat-sheet
 Simple quick tips and trick to JS

## 1.Remove duplicates from array
```
let animles = ["tiger", "rat", "lion", "frog", "monkey", "bird", "cat", "lion", "frog"]


// First method
var uniqueAnimles = Array.from(new Set(animles));
console.log(uniqueFruits); // returns ["tiger", "rat", "lion", "frog", "monkey", "bird", "cat"]

// Second method
var uniqueAnimles2 = […new Set(animles)];

console.log(uniqueAnimles2); // returns ["tiger", "rat", "lion", "frog", "monkey", "bird", "cat"]
```

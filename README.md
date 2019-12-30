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

## 2.Replace a specific value in array

```
var fruits = [“banana”, “apple”, “orange”, “watermelon”, “apple”, “orange”, “grape”, “apple”];
fruits.splice(0, 2, “potato”, “tomato”);
console.log(fruits); // returns [“potato”, “tomato”, “orange”, “watermelon”, “apple”, “orange”, “grape”, “apple”]
```

## 3.Empty an array
```
let animles = ["tiger", "rat", "lion", "frog", "monkey", "bird", "cat"]

animles.length = 0
console.log(animles) // returns []
```

## 4.Convert array to an object
```
let animles = ["tiger", "rat", "lion", "frog", "monkey", "bird", "cat"]
let obj = { ...animles }
console.log(obj) // returns { 0: "tiger", 1: "rat" ...}
```

## 5.Fill array with data
```
let arr = new Array(5).fill(“1”)
console.log(arr) // returns ["1", "1", "1", "1", "1"]
```

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

## 6.Find the intersection between 2 arrays
### Option 1:
```
var numOne = [0, 2, 4, 6, 8, 8];
var numTwo = [1, 2, 3, 4, 5, 6];
var duplicatedValues = […new Set(numOne)].filter(item => numTwo.includes(item));
console.log(duplicatedValues); // returns [2, 4, 6]
```
### Option 2:
```
let firstValues = new Set(numOne);
let duplicatedValues = numTwo.filter(item => firstValues.has(item));
```

## 7.Remove falsy values from an array
```
var mixedArr = [0, “blue”, “”, NaN, 9, true, undefined, “white”, false];
var trueArr = mixedArr.filter(Boolean);
console.log(trueArr); // returns [“blue”, 9, true, “white”]
```

## 8. For loop in - For Objects
```
let obj = { a: 1, b: 2, c: 3}
for (let i in obj) {
  console.log(i, obj[i])
}
```
## 9. For loop of - For Arrays
```
let arr = [1, 2, 3, 4, 5]
for (let i of arr) {
  console.log(i)
}
```

## 10.Delete element in array
```
myArray.splice(target_index,number_of_elements)
```

## 11.Set Operations
```
// 27. Set Operations: isSuperSet
function isSuperset(set, subset) {
    for (let elem of subset) {
        if (!set.has(elem)) {
            return false;
        }
    }
    return true;
}
// 28. Set Operations: union
function union(setA, setB) {
    let _union = new Set(setA);
    for (let elem of setB) {
        _union.add(elem);
    }
    return _union;
}

// 29. Set Operations: intersection
function intersection(setA, setB) {
    let _intersection = new Set();
    for (let elem of setB) {
        if (setA.has(elem)) {
            _intersection.add(elem);
        }
    }
    return _intersection;
}
// 30. Set Operations: symmetricDifference
function symmetricDifference(setA, setB) {
    let _difference = new Set(setA);
    for (let elem of setB) {
        if (_difference.has(elem)) {
            _difference.delete(elem);
        } else {
            _difference.add(elem);
        }
    }
    return _difference;
}
// 31. Set Operations: difference
function difference(setA, setB) {
    let _difference = new Set(setA);
    for (let elem of setB) {
        _difference.delete(elem);
    }
    return _difference;
}

// Examples
let setA = new Set([1, 2, 3, 4]);
let setB = new Set([2, 3]);
let setC = new Set([3, 4, 5, 6]);

console.log(isSuperset(setA, setB));            // => true
console.log(union(setA, setC));                 // => Set [1, 2, 3, 4, 5, 6]
console.log(intersection(setA, setC));          // => Set [3, 4]
console.log(symmetricDifference(setA, setC));   // => Set [1, 2, 5, 6]
console.log(difference(setA, setC));            // => Set [1, 2]
```


# 0x03. ES6 data manipulation
Welcome to the ES6 Data Manipulation repository! In this guide, you'll learn how to leverage the power of ES6 features for efficient data manipulation. This README covers the usage of map, filter, and reduce methods on arrays, working with Typed Arrays, and understanding Set, Map, and WeakLink data structures.

## Table of Contents
- Using map, filter, and reduce on Arrays
- Typed Arrays
- Set, Map, and WeakLink Data Structures
## Using map, filter, and reduce on Arrays <a name="array-methods"></a>
ES6 introduced powerful array methods: map, filter, and reduce. Here's how you can use them:

### 1. map()
map() creates a new array by applying a function to each element of the original array.

```
const numbers = [1, 2, 3, 4, 5];
const squaredNumbers = numbers.map(num => num * num);
console.log(squaredNumbers); // Output: [1, 4, 9, 16, 25]
```

2. filter()
filter() creates a new array with elements that pass the test implemented by the provided function.

```
const numbers = [1, 2, 3, 4, 5];
const evenNumbers = numbers.filter(num => num % 2 === 0);
console.log(evenNumbers); // Output: [2, 4]
```

3. reduce()
reduce() applies a function against an accumulator and each element in the array (from left to right) to reduce it to a single value.

```
const numbers = [1, 2, 3, 4, 5];
const sum = numbers.reduce((accumulator, currentValue) => accumulator + currentValue, 0);
console.log(sum); // Output: 15
```

## Typed Arrays <a name="typed-arrays"></a>
Typed Arrays provide a way to work with binary data in the form of arrays of various numeric types.

```
// Create a 32-bit integer typed array with length 5
const intArray = new Int32Array(5);
intArray[0] = 1;
intArray[1] = 2;
intArray[2] = 3;
intArray[3] = 4;
intArray[4] = 5;

console.log(intArray); // Output: Int32Array [ 1, 2, 3, 4, 5 ]
```

## Set, Map, and WeakLink Data Structures <a name="data-structures"></a>
1. Set
A Set is a collection of unique values.

```
const uniqueNumbers = new Set([1, 2, 3, 4, 4, 5, 5]);
console.log(uniqueNumbers); // Output: Set { 1, 2, 3, 4, 5 }
```


2. Map
A Map is a collection of key-value pairs.

```
const person = new Map();
person.set('name', 'John');
person.set('age', 30);

console.log(person.get('name')); // Output: John
console.log(person.get('age'));  // Output: 30

```

3. WeakLink
A WeakLink is a collection of key-value pairs where keys are weakly referenced.

```
let weakLink = new WeakMap();

let element = document.getElementById('example');
weakLink.set(element, 'Metadata associated with the element');

```

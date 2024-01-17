some usage of spread operator

```js
/**
* 1. function calls when pass multiple parameters
*/

const arr1 = [1, 2, 3];
const sum = (x, y, z) => {
  return x + y + z;
};

sum(...arr1); // output -> 6

//2. array literals
const arr2 = [1, 2, 3];
const arr3 = [4, 5, 6];

const arr4 = [...arr2, ...arr3];
// output -> [1,2,3,4,5,6]


// 3. objetc literals
const obj1 = {
  name: "John",
  age: 30,
};

const obj2 = {
  ...obj1,
  address: "New York",
};

obj2; 
// output -> {name: 'John', age: 30, address: 'New York'}

// 4. shallow copy
// primitive type copy by value and object copy by reference
const arr5 = [1, 2, { a: 3 }];
const arr6 = [...arr5];
console.log(arr6); // output [1,2, {a:3}]

arr5[2].a = 33;
console.log(arr6);
// output [1,2,{a:33}]


// 5. destructuring
const [first, ...left] = [1, 2, 3, 4, 5];
first; // output -> 1
left; // output -> [2,3,4,5]

// 6. strings to chars
const str = "java"
const chars = [...str] // output ['j', 'a', 'v', 'a']
```



[  
](/**%0A*%201.%20function%20calls%20when%20pass%20multiple%20parameters%0A*/%0A)

[  
](/**%0A*%201.%20function%20calls%20when%20pass%20multiple%20parameters%0A*/%0A)

[  
](/**%0A*%201.%20function%20calls%20when%20pass%20multiple%20parameters%0A*/%0A)


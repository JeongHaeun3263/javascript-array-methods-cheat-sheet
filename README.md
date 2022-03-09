# JavaScript Array Methods Cheat Sheet

```
const arr = [1, 3, 5, 7];
const arr2 = [1, 3, 5, 5, 7];
const arr3 = ['d', 'a', 'b', 'c'];
const arr4 = [1, 30, 2, 100];
const users = [
	{ name: 'grace', city: 'Toronto', age: 30 },
	{ name: 'monica', city: 'New York', age: 24 },
];
```

| Method        | Code Example                                                                                                                        | Result                                                      | Return Type    | In Place |
| ------------- | ----------------------------------------------------------------------------------------------------------------------------------- | ----------------------------------------------------------- | -------------- | -------- |
| keys()        | const iterator = arr.keys(); <br> for (const key of iterator) { <br> console.log(key);<br> }                                        | 0 <br> 1 <br> 2 <br> 3                                      | Array Iterator | No       |
| values()      | const iterator = arr.values(); <br> for (const value of iterator) { <br> console.log(value); <br> }                                 | 1 <br> 3 <br> 5 <br> 7                                      | Array Iterator | No       |
| push()        | console.log(arr.push(9)); <br> console.log(arr); <br>                                                                               | 5 // new length of the array <br> [1, 3, 5, 7, 9]           | number         | No       |
| pop()         | console.log(arr.pop()); <br> console.log(arr);                                                                                      | 7 // last element of the array <br> [1, 3, 5]               | element        | No       |
| shift()       | console.log(arr.shift()); <br> console.log(arr);                                                                                    | 1 // removed element <br> [3, 5, 7]                         | element        | No       |
| unshift()     | console.log(arr.unshift(2, 4)); <br> console.log(arr);                                                                              | 6 // new length of the array <br> [2, 4, 1, 3, 5, 7]        | number         | No       |
| slice()       | console.log(arr.slice(1, 3)); <br> console.log(arr); <br> // remain from index 1 to 2 (last one is not included)                    | [3, 5] <br> [ 1, 3, 5, 7 ]                                  | array          | No       |
| splice()      | arr.splice(1, 0, 2); // insert ‘2’ at index 1 <br> console.log(arr);                                                                | [1, 2, 3, 5, 7]                                             | array          | Yes      |
| splice()      | arr.splice(3, 1, 4); // replace 1 item at index 3 <br> console.log(arr);                                                            | [1, 3, 5, 4]                                                | array          | Yes      |
| splice()      | console.log(arr.splice(1, 2)); // remove 2 items from index 1 <br> console.log(arr);                                                | [3, 5] // removed items <br> [1, 7] // array as a result    | array          | Yes      |
| join()        | console.log(arr.join());                                                                                                            | 1,3,5,7                                                     | string         | No       |
| indexOf()     | console.log(arr.indexOf(3));                                                                                                        | 1                                                           | number         | No       |
| lastIndexOf() | console.log(arr2.lastIndexOf(5));                                                                                                   | 3                                                           | number         | No       |
| reduce()      | console.log(arr.reduce((pre, curr) => pre + curr));                                                                                 | 16                                                          | number         | No       |
| find()        | console.log(arr.find((num) => num > 3));                                                                                            | 5                                                           | first one      | No       |
| findIndex()   | console.log(arr.findIndex((num) => num > 3));                                                                                       | 2                                                           | first one      | No       |
| every()       | console.log(arr.every((num) => num % 2 === 1));                                                                                     | TRUE                                                        | boolean        | No       |
| every()       | console.log(arr.every((num) => num > 10));                                                                                          | FALSE                                                       | boolean        | No       |
| some()        | console.log(arr.some((num) => num > 5));                                                                                            | TRUE                                                        | boolean        | No       |
| filter()      | console.log(arr.filter((num) => num > 3)); <br> const newUsers = users.filter((user) => user.age > 25); <br> console.log(newUsers); | [5, 7] <br> [ { name: 'grace', city: 'Toronto', age: 30 } ] | array          | No       |
| map()         | arr.map((item) => item \* 2) <br> users.map((user) => console.log(user.name));                                                      | [2, 6, 10, 14] <br> grace <br> monica                       | array          | No       |
| flatMap()     | console.log(arr.flatMap((x) => [x, x \* 2]));                                                                                       | [1, 2, 3, 6, 5, 10, 7, 14]                                  | array          | No       |
| forEach()     | arr.forEach((item) => console.log(item \* 2));                                                                                      | 2 <br> 6 <br> 10 <br> 14                                    | each element   | No       |
| includes()    | console.log(arr.includes(3));                                                                                                       | TRUE                                                        | boolean        | No       |
| isArray()     | console.log(Array.isArray([1, 2, 3]));                                                                                              | TRUE                                                        | boolean        | No       |
| reverse()     | console.log(arr.reverse());                                                                                                         | [7, 5, 3, 1]                                                | array          | Yes      |
| concat()      | const newArr = arr.concat(['a', 'b']); <br> console.log(newArr);                                                                    | [1, 3, 5, 7, "a", "b"]                                      | array          | No       |
| fill()        | console.log(arr.fill('a', 1, 3)); <br> // fill with 'a' from position 1 until position 3                                            | [1, "a", "a", 7]                                            | array          | No       |
| flat()        | const newArr = [1, 3, 5, 7, [2, 4]]; <br> console.log(newArr.flat());                                                               | [1, 3, 5, 7, 2, 4]                                          | array          | No       |
| Array.from()  | console.log(Array.from([1, 2, 3], (x) => x \* 2));                                                                                  | [2, 4, 6]                                                   | array          | No       |
| Array.from()  | console.log(Array.from('grace'));                                                                                                   | ["g", "r", "a", "c", "e"]                                   | array          | No       |
| sort()        | console.log(arr3.sort());                                                                                                           | ["a", "b", "c", "d"]                                        | array          | Yes      |
| sort()        | console.log(arr4.sort()); <br> console.log(arr4.sort((a, b) => a - b));                                                             | [ 1, 100, 2, 30 ] <br> [1, 2, 30, 100]                      | array          | Yes      |

```

```

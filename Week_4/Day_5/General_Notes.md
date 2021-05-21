## Notes

#### ALGORITHMS

- What is an Elementary Operation?
  - An elementary operation is any oepration that takes a fixed amount of time to perform such as

  ``` js
  // running time is 1
  number1 + number2;
  
  // running time is 1
  console.log(someString);

  // running time is 4
  let result = 0;
  result += number1;
  result += number2;
  console.log(result);
  ```

- An algorithm is any piece of code that performs a particular task or solves a particular problem
- Time complexity is commonly estimated by counting the number of elementary operations performed by an algorithm. It takes a fixed amount of time to perform an elementary operation.
- Time complexity is often referred to as running time
- Algorithms that don't deal with dynamic data, like loops, usually take constant time (no n involved)
- Algorithms that iterate over data, involve using n based on the size of the data

``` js
let result = 0;

for (let i = 0; i < array.length; i++) {
  let number = array[i];
  result += number;
}

console.log(result);
```
- This algorithm takes 4n + 4 time to complete
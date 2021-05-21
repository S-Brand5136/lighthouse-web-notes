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

```js
let result = 0; // 1

for (
  let i = 0; // 1
  i < array.length; // n + 1
  i++ // n
) {
  let number = array[i]; // n
  result += number; // n
}

console.log(result); // 1
```

## Linear vs Logarithmic Algorithms

- Learning Outcomes
  - can understand what binary search is
    - Binary search is an efficient way of finding a value from a sorted list by halving the possible number of values in half until the requested value is found
  - can identify when and why to use binary search
    - Binary search algorithms are useful when you already have a a sorted list of items
  - can analyze a binary search on an array of ordered elements
  - can compare time complexity for linear vs binary search
    - Linear search time complexity is n while bineary search is log2n
  - can determine and use worst case scenario for determining complexity
    - Worst case scenario for binary search is how many times the algoirthm has to go through the data set to find out it doesn't contain what its looking for. this can be found by finding out the log2n = x equation and adding the base amount of elementary operations. for 1000 items its 93 operations.
  - can understand that if the input data for an algorithm doubles in size, and the   number of steps only increases by one, then the algorithm's running time is logarithmic


Here's a step-by-step description of using binary search to play the guessing game:
 - Let min = 1min=1m, i, n, equals, 1 and max = nmax=nm, a, x, equals, n.
Guess the average of maxmaxm, a, x and minminm, i, n, rounded down so that it is an integer.
 - If you guessed the number, stop. You found it!
 - If the guess was too low, set minminm, i, n to be one larger than the guess.
 - If the guess was too high, set maxmaxm, a, x to be one smaller than the guess.
Go back to step two.

## Quadratic

Learning Outcomes
- can identify the difference between linear and quadratic time
  - Quadratic time is when an algorithms performance is proportional to the squared size of the input data set. O(N2) so O(2(2)) = 4. if it was Linear time where the longest run time is equal to n, the amount of data passed in. it would just be O(n) or O(2) = 2. quadratic time gets worse and worse when you add in larger and larger datasets. While linear time does exactly what the name says. stays linear.

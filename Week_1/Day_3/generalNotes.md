### Tips

- A good way to iterate through an object is to use the `for..in` loop. How ever it can produce unexpected results, additional checks may be needed. It also only iterates over enumerable, non-Symbol properities.

  ```javascript
  for(values in object) {
    console.log("value = ", value)
    <!-- This will iterate through the object printing 
         each value to the console -->
  }
  ```
- `for..in` is *not recommended* for iterating over arrays. `forEach()` or `for..of` is recommended


#### Quiz learning outcome questions

- Can access an element in a nested associative array


- Can list the primitive datatypes in their language

- Can access an element in an associative array
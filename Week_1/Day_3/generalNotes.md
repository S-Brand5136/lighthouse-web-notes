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
  - to access an element in a nested associative array

  ```javascript
    const obj = {
      arrayOne: [1,2,3, [4,5,6]],
      arrayTwo: [1,2,3,4]
    }
    console.log(obj["arrayOne"][3][2]) // -> 6

  ```

- Can list the primitive datatypes in their language
  - Javascript has 7 primitive types 
      - Boolean
      - Number
      - String
      - Undefined
      - Null
      - Big Int
      - Symbol

- Can access an element in an associative array
```javascript
  const myObj = {
    one: '1'
    two: '1'
  }
  console.log(myObj.one) // -> "1"
```
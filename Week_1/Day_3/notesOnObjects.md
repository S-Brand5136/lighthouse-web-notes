## Objects at a glance

 - Objects
    - Contain `Key-value` pairs; each key maps to a value
    - Contain Keys which are `always strings`
    - Have `unique keys`; the same key `cannot appear twice` in an object
    - Have their keys `point to values` which can be of any type
  

- Object Literals
   - Objects have a literal syntax using braces {}

    ```javascript
        const tinyObject = {"size": "Tiny};
    ```
   
   - The object has a single key (size) and an associated value (Tiny)

- Objects are like 2 column tables
  -the `key` and the `value` can be thought of as two seperate columns

- Object keys
  - Keys are always strings
  - Each key is unique
  - Each key is associated with exactly one value (technically the value can be an object or array as well)

  - When writting out an object literal the key is `always` interpereted as a `literal string` even if its unqouted

  ```javascript
    const myObject = { myKey: "the value" };
  ```

  - it is only neccesary to put quotes around a key that has spaces, hyphens, periods etc

  - The following is an `example` showing two ways of specifiying the same *value* in an object literal; using a `literal string` for the value or a `variable`.

  ```javascript
  const spam = "spam"; // Variable spam is made
  person["dislikes"] = { food: spam, "e-mail": "spam"}
  ```
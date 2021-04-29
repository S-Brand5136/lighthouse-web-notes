
#### Primitive types don't have *Properties* but they do have *corresponding objects*
  - Each primitive (excluding `*Symbol*`) has an `object constructor`
  ```javascript
  typeof(true); 
  // "boolean" 
  typeof(Boolean(true)); 
  // => "boolean" 
  typeof(new Boolean(true));
  // => "object"
  /*  
  It is generally considered bad practice to use primitive object constructors (as shown in the final line above). 
  */
  ```

  - when *methods* are called on `primitive data` types Javascript will use *type-coercion* to convert them to its corresponding object

```javascript
  const greeting = "Hello, world!" 
  const objGreeting = new String("Hello, world!");

  greeting == objGreeting; 
  // => true

  greeting === objGreeting; 
  // => false
```

  - Here we can see that a `primitive string` is -*not*- the same as an `Object string`
  
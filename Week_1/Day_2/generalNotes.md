### Tips

#### Problem solving

- List out the problems your trying to solve

- Restating a problem and then breaking it up into `pseudocode` is a great way to finding out a solution

- `Experiment` with a reduced version of the problem

- Solve the parts that are the `most obvious first`, and try to get the `simpliest solution` working

- Look for `analogies`. Two problems can look entirely different but require the same solution.

- Trying to solve the part of the problem with the most constraints can help `simplify the problem` by eliminating possible choices.

- Figure out the expected out come of the problem. It may not be immediately obvious at first

### Eloquent Javascript

- If its hard to define a name for a function its more then likely taking on too much responsibility

- Stick to the `DRY`(Don't repeat yourself) method of coding. It forces modularity

- Adding `nice` and `obvious` names to functions makes it easier for someone who reads the code to figure out what it does

- Don't add clerverness unless you are absolutely going to need it

### Functions and side effects

- Functions can be roughly split into two groups. Functions that are called for their `side effects` and those for their `return values`

- `pure` functons are specific kinds that don't relay on side effects and also doesn't create any side effects. It `always produces the same value`.

### Conventions for Functions

- Avoid generic names
- Name functions with actions words
- Use `camelCase` when writting function names unless otherwise specified
- `Indentation` is key
- be `consistent` with your conventions
- observe and adapt any existing naming conventions
- Functions should ideally not read outter scoped variables, it should be passed in

- Functions should `focus on a single task`. returning a value or causing a side effects

- _Break your functions into `additional smaller functions` if you find it doing two or more things_

### Day 2 Quiz learning outcomes

#### _List and explain various multi-word naming conventions_

- camelCase

  - Is one of the more popular name conventions. the first letter is lower case and every word after starts with a capital

  ```javascript
  const camelCase = "thisIsCamelCase";
  ```

- snake_case

  - each word is seperated by an underscore. No capitals are used. JSON uses it

  ```JSON
    "first_name": "Brandon",
    "last_name": "Shemilt",
  ```

- kebob-case
  - each word is seperated by a hyphon. No capitals. Found a lot in HTML and CSS
  ```HTML
    <p id="personal-greeting">Hello World</p>
  ```

### _Can explain what type coercion is_

- Type coercion is converting one variable type to another. This is used a lot in javascript when comparing variable types for truthy or falsey values

  - article from [FreeCodeCamp](https://www.freecodecamp.org/news/js-type-coercion-explained-27ba3d9a2839/)
  - Stack overflow [Answer](http://stackoverflow.com/questions/359494/does-it-matter-which-equals-operator-vs-i-use-in-javascript-comparisons/359509#359509)

  ```javascript
  if (3 == "3") {
    console.log("True"); // true
  }

  let name = "";

  if (!name) {
    // empty strings are a falsey value so the if statement executes
    name = "Brandon";
  }
  ```

### Understand the difference between "==" and "==="

- javascript will try and force type coercion on an expression using "=="

  ```javascript
    if(3 == "3") // both values will be converted to the same type
  ```

- javascript will check for the same variable types when using '==='

  ```javascript
    if(3 === '3') // will return false, different variable types
  ```

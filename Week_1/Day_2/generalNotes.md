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
- Use camelCase when writting function names unless otherwise specified
- Indentation is key
- be consistent with your conventions
- observe and adapt any existing naming conventions
- Functions should ideally not read outter scoped variables, it should be passed in

- Functions should focus on a single task. returning a value or causing a side effects

- _Break your functions into `additional smaller functions` if you find it doing two or more things_

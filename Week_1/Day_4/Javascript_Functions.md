### Javascript Functions as objects

* Functions are *First-class objcets*

  - Functions can be stored `inside of variables` as well as `passed around`
  - Functions can do `everything` that other objects can do

- The most useful characteristic of having a function as a value is using it as a callback function

#### Call back functions

  - Is a function *passed* by `reference` into another function
  - The *reciever* function is taking in the behavior to perform by *calling* the `callback`
  - The *reciever* function decides if it is going to *call* the `callback function` and how many *times*

### Function Notes
  - Functions that take *in callbacks* are referred to as `Higher Order Functions`,
  or in other words `Higher-Order Functions` are any functions which operate on other functions

    - In even simpler words `Higher-Oder Functions` are functions that either take in a function as an `argument` or returns a function as `output`

    - examples of higher order functions are .map(), .filter(), .forEach()


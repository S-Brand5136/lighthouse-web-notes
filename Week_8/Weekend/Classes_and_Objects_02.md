# Classes and Objects II

- Class Methods

  - Class methods are methods that we can call directly on the class itself, without needing to instantiate any objects

  - When defining a class method we prepend the method name with the reserved word self.

- Class Variables

  - Class variables are created using double `@@`
  - Class variables pretain to only the class itself and not too objects instatiated from that class

- Constants

  - To declare a constant, add an Uppercase letter to the begining of the variable name. Most ruby developers put the name in all upper case

- `to_s` method

  - Is called automatically on the object when we use it with puts or with string interpolation.
  - We can define it in the class to give a more descripitive output

- More about self

  - For example, so far we've seen two clear use cases for self:

    1. Use self when calling setter methods from within the class. In our earlier example we showed that self was necessary in order for our change_info method to work properly. We had to use self to allow Ruby to disambiguate between initializing a local variable and calling a setter method.

    2. Use self for class method definitions.

  - calling self.name= acts the same as calling sparky.name=

  - When self is prepended to a method definition, it is defining a class method.

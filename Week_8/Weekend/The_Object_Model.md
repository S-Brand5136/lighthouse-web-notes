## The object model

- Encaspulation

  - Is hiding pieces of functionality and making it unavailable to the rest of the code base.
  - It works as a form of data protection, so that data can be manipulated or changed without obvious intention
  - It defines boundarys within a code base and lets you create more complex apps

- Polymorphism

  - gives the ability for different data types to respond to a common interface.
  - If there is a method that expects argument objects that are the same across multiple classes we can pass it any type of argument, provided it has a compatiable method.
  - Polymorphism gives the flexiability to use pre-written code in new ways
  - One way to apply a polymorphic strucutre in Ruby is to use a module. They work similar to a class, in that they contain shared behavior. However you cannot create a module in an object. They have to be used as a mixin by using include method invocation.

- Objects

  - Ruby defines the attributes and behaviors of its objects in classes.
  - Classes can be thought of as basic outlines of what an object should be made of and what it should be able to do.
  - Classes are defined similarily to defining a method.

  ```Ruby
    class GoodDog
    end

    spark = GoodDog.new
  ```

  - The camelcase naming convention is used to create class names

  - all Class definitions must end with the keyword end

  -

- Modules

  - A module is a collection of behaviors that is usable in other classes via mixins
  - A module is mixed in to a class using the `include` method incovation.
  -

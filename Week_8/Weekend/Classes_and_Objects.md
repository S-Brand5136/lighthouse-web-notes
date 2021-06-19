# Classes and Objects

- States and Behaviors

  - States track attributes for individual objects.
  - Behaviors are what objects are capable of doing

  - instance variables keep track of state, and instance methods expose behavior for objects.

- Initializing a New objec

  - The `initialize` method gets called everytime you create a new object.
  - The `initialize` method is a constructor in Ruby, and just like in other languages it gets triggered whenever new objects are created.

- Instance Variables

  - Instance variables in Ruby start with an `@`.
  - Instance variables exist as long as the object instance exists, and its is one of the ways data is tied to objects
  - It lives on until the object is destroyed
  - arguments are passed into the `initialize` method through the `new` method.

  - Every objects state is unique, and instance variables are how to keep track of it

- Accsessor Methods

  - Acccessor Methods are ways to get and set an objects variables

  ```Ruby
    class GoodDog
    attr_accessor :name

    def initialize(name)
    @name = name
    end

    def speak
    "#{@name} says arf!"
    end
    end

    sparky = GoodDog.new("Sparky")
    puts sparky.speak
    puts sparky.name # => "Sparky"
    sparky.name = "Spartacus"
    puts sparky.name # => "Spas
  ```

- The attr_accessor method creates getters and setters for us

- If we only want the getter without the setter method we can use `attr_reader`

- If we only want the setter method we can use `attr_writer`

```Ruby
  # - This is how to set multiple getters and setters with attr_accessor
attr_accessor :name, :height, :weight
```

- Calling Methods with self

  - To disambiguate from creating a local variable, use the `self` keyword. It works like `this` in other languages where it refers to an objects variable

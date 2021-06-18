# Notes

- Ruby files end with .rb and can be executed with the keyword ruby on the command line

- By convention use snake_case for variable names

```bash
  $ ruby example.rb
```

- The keyword **puts** prints to the console with a new line
- The keyword **prints** prints to the console without a new line

```ruby
  puts "Hello World"
```

- Like Node with npm, Ruby also has a package manager and it can be used with the **gem** command. Ruby packages are called **gems**

```bash
  $ gem list
  // This prints out all the globally installed gems
```

## Comments

```rb
  # This is a comment

  =begin
    This is a multiline comment in ruby
  =end
```

## Objects

- In Ruby almost everything is an object. This includes Numbers

```ruby
  # Numbers
  3.class #=> Integer

  # Strings
  "Hello".class #=> String

  # Methods
  "Hello".method(:class).class
```

- Special values are objects

```ruby
# Special values are objects

nil # equivalent to null in other languages
true # truth
false # falsehood

nil.class #=> NilClass
true.class #=> TrueClass
false.class #=> FalseClass
```

## Bit wise operators

```ruby
  # Bitwise operators
3 & 5 #=> 1
3 | 5 #=> 7
3 ^ 5 #=> 6
```

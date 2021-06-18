# Notes

## Ruby

- Information on how to use the yeild keyword [Stackover Flow](https://stackoverflow.com/questions/3066703/blocks-and-yields-in-ruby)

#### Blocks

- **block** and **yield** are ways to pass behavior into a def in ruby
- When passing behavior we have to put it inbetween curly braces when we call the method

  - There is a couple ways to accomplish this

```ruby
  # Concept 1
    def print_result
      result_from_block = yield
      puts result_from_block
    end

    # This will print 9 to the console
    print_result{ 3 * 3}

  # Concept 2
  def print_result(&block)
    result_from_block = block.call
    puts result_from_block
  end

  # This will also print 9 to the console
  print_result{ 3 * 3 }
```

- Blocks in ruby act very similar to callbacks in javscript

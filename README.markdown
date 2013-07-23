# RubyBuffer

> execute selected ruby and return the result in a scratch buffer

### How To:

It's easy:
- Make sure the buffer has it's filetype set to ruby:
  - `:set ft=ruby`
- Visually select some ruby code, or don't and the whole file will be used
- `:RubyBuffer`
- Any writes to standard out, and the last line of your script will be put into a new scratch buffer
- Optionally map it to something sweet, like `map <leader>r :RubyBuffer <cr>`

### Example:

````
puts "I go to standard out"
class MyClass
  def self.one_plus_one
    1+1
  end
end

MyClass.one_plus_one
````

Will create a new scratch buffer containing:

````
I go to standard out
2
````

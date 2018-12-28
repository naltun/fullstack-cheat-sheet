# Full Stack Cheat Sheet

### The _what_
This is a cheat sheet for Full Stack developers of all skill levels, including both our aspiring and experienced developers in the community.

### License
This documentation is licensed under the terms of the Creative Commons _**Attribution-ShareAlike 4.0 International (CC BY-SA 4.0)**_ license. This means you can do _whatever_ you want with this document, _**as long as**_ you provide credit to the author (me). 

![CC BY-SA 4.0 License](https://licensebuttons.net/l/by-sa/4.0/88x31.png)

Love your Free/Libre, Open Source Software. For more information, please visit [Wikipedia](https://en.wikipedia.org/wiki/Free_software_movement).

Likewise, support [Free Culture](https://creativecommons.org/share-your-work/public-domain/freeworks).

------

### Table of Contents
1) Ruby
2) JavaScript
3) HTML
4) CSS

### Ruby
#### What we'll learn
* Variables
* Operators
* Conditionals
* Loops
* Methods

##### Variables
A variable is a named reference to a value. These values can be of different data types or objects of Classes.

Example:
```ruby
name = 'Noah'
age = 27
panda = false
```

Variables can be reassigned values:
```ruby
job = 'Scientist'
job = 'Museum Curator'
puts job # => "Museum Curator"
```

Constants are like variables, except the values cannot be changed:
```ruby
FAV_FOOD = 'Pizza'
FAV_FOOD = 'Hotdogs' # => warning: already initialized consant FAV_FOOD
```

##### Operators
An operator in Ruby is a symbol that takes two or more values and performs some _operations_ on them. Some operators are:
* \+
* \-
* \*
* \/

Let's use these in an example:
```ruby
puts 1 + 2 # => 3
puts 5 - 3 # => 2
puts 2 * 6 # => 12
puts 10 / 2 # => 5
```

We can also use operators on strings:
```ruby
name = 'Noah'
puts name * 5 # => "NoahNoahNoahNoahNoah"
```

Ruby also has comparison operators for performing conditionals:
* \==
* \!=
* \>
* \<
* \>=
* \<=
* \<=>
* \===

For more information on conditionals, please refer to the Ruby conditional's section!

##### Conditionals
`IF...ELSIF...ELSE`, the 3 keywords for performing Ruby conditionals.

Ruby conditionals let us execute code based on conditions in our code. 
Let us consider this example:

```ruby
country = 'US'
if country == 'UK'
  puts 'Person is British!'
elsif country == 'US'
  puts 'Person is American!'
else
  puts 'Person is not from the UK or the US!'
end
# => "Person is American!"
```

Ruby allows us do to sweet one-liners. This is recommended for devs with some experience. Let's look at some examples:
```ruby
age = 22
puts 'Person is not a teenager!' if age >= 20
```

##### Methods
A method is a named reference for reusable code. This can either be predefined with Ruby, or user-defined.

In example:
```ruby
puts 'Hello, World!' # => "Hello, World!"
```

We also have methods with dot notation:
```ruby
'Ruby rocks'.length # => 10
```

Here is an example of a user-defined method:
```ruby
def hello(name = 'World!')
  puts "Hello, #{name}!"
end

hello # => "Hello, World!"
hello('Steve') # => "Hello, Steve!"
```

Let's take a look at a more complex example:
```ruby
require 'base64'

def hex_to_base64(hex)
  hex_str_unencoded = [hex].pack('H*')
  hex_str_as_bytes = hex_str_unencoded.bytes

  base64_str_unencoded = hex_str_as_bytes.pack('c*')
  base64_str_encoded = Base64.strict_encode64(base64_str_unencoded)

  return base64_str_encoded
end

hex_to_base64('49276d206b696c6c696e6720796f757220627261696e206c696b65206120706f69736f6e6f7573206d757368726f6f6d') # => "SSdtIGtpbGxpbmcgeW91ciBicmFpbiBsaWtlIGEgcG9pc29ub3VzIG11c2hyb29t"
```

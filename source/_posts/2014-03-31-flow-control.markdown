---
layout: post
title: "Flow Control"
date: 2014-03-31 22:19:22 +0800
comments: true
categories: [CH3] 
---

*started from P. 59*

Conditions controls are able to be nested.

- `if` and `unless`
- `?` and Ternary Operator
- `elseif` and `case`
- `while` and `until`
- code blocks

<!-- more -->

### `if` and `unless`

- `unless` is just the oppsite of `if`
- both support `else` condition
  - `end` put at after the full control flow.

```ruby
age = 10
if age < 18
 puts "You are too young"
else
 puts "You are good"
end
```

and

```ruby
age = 10
unless age > 18
 puts "You are too young"
else
 puts "You are good"
end
```

will both get

```sh
You are too young
```

### `?` and Ternary Operator

#### Basic Pattern

```text
<condition> ? <result if condition is true> : <result if condition is false>
```

##### Example

```ruby
age = 10
puts "You are a " + (age < 18 ? "child" : "adult")
```

will get

```sh
You are a child
```

### `elseif` and `case/when`

#### `elseif`

```ruby
if <condition>
 <statement>
elseif <condition>
 <statement>
else
 <statement>
end
```

##### Example

```ruby
fruit = "orange"
if fruit == "orange"
 color = "orange"
else if fruit == "apple"
 color = "red"
else
 color = "unknown"
end
```

#### `case/when`

```ruby
case <target>
 when <condition>
 <statement>
 when <condition>
 <statement>
 else
 <statement>
end
```

##### Example

```ruby
fruit = "orange"
color = case fruit
 when "orange"
 "orange"
 when "apple"
 "red"
 else
 "unknown"
end
```
#### `while` and `until`

`while` and `until` can loop the code based on the given condition.

##### `while`

```ruby
x = 1
while x < 100
 puts x
 x = x * 2
end
```

will get

```sh
1
2
4
8
16
32
64
```

##### `until`

`until` provide the opposite functionality

```ruby
x = 1
until x > 99
 puts x
 x = x * 2
end
```

will get the same result like `while`'s

```sh
1
2
4
8
16
32
64
```

##### More Like English

As `if` and `unless`, you can do `while` and `until` literally.

```ruby
i = 1
i = i * 2 until i > 1000
puts i
```

will get

```sh
1024
```

### Code Blocks 

Code blocks is defined within `{` and `}` or `do` and `end` delimiters.

More advance, you can write methods with your own handled blocks:

```ruby
def each_vowel(&code_block)
 %w{a e i o u}.each { |vowel| code_block.call(vowel) }
end

each_vowel { |vowel| puts vowel }
```

will get

```sh
a
e
i
o
u
```

- `%w` is literal for `Arrays` ([ref](http://www.zenspider.com/Languages/Ruby/QuickRef.html#arrays))
- `.call()` is a method of `Proc` class, given parameter(s) will be used in the code block given.

#### `lambda`

`lambda` is a method from `Kernal`, it return a `Proc` object. [The difference between both](http://awaxman11.github.io/blog/2013/08/05/what-is-the-difference-between-a-block/).

```ruby
print_something = lambda { |x| puts x}
print_something.call(100)
```

will get

```sh
100
```

### References

- [`Proc`](http://www.ruby-doc.org/core-2.1.1/Proc.html#method-i-call)
- [`Proc.call()`](http://www.ruby-doc.org/core-2.1.1/Proc.html)
- [`Array` literal](http://www.zenspider.com/Languages/Ruby/QuickRef.html#arrays)
- [`Kernal.lambda`](http://www.ruby-doc.org/core-2.1.1/Kernel.html#method-i-lambda)

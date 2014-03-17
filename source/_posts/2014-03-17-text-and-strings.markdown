---
layout: post
title: "Text and Strings"
date: 2014-03-17 22:43:52 +0800
comments: true
categories: [CH3] 
---

*start from P. 39*

Manipulating text and content.

- String Literals 

<!-- more -->

## String Literals

First, the `String` class:

```ruby
puts "Hello, world!".class
```

will get

```sh
String
```

### Basic expressions just like `Number`s

```ruby
x = "Test"
y = "String"
puts "Success!" if x + y == "TestString"
```

result:

```sh
Success!
```

### Multiple Lines

You can wrap your lines with your prefered delimiters.

```ruby
x = %q{This is first line,
second line and
third line}

// or

x = %q!This is first line,
second line and
third line!

// or

x = <<END_MY_LINE
This is first line
second line and
third line
END_MY_LINE

```

For the last example above, << start the string literal.

### String Expressions

Just like the previous section, `String` could use expressions and act like `Number`.

```ruby
puts "abc"*5
// abcabcabcabcabc

puts "x" > "y"
// false

puts "y" > "x"
// true
```

#### ASCII

```ruby
puts ?x
puts 120.chr
```
First line will convert character to `ASCII` value, the second line will convert the value to character based on `ASCII`:
```sh
120
x
```

## References

- class [String](http://www.ruby-doc.org/core-2.1.1/String.html) *base on ruby 2.1.1*

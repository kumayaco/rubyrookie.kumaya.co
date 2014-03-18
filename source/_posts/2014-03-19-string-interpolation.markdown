---
layout: post
title: "String: Interpolation"
date: 2014-03-19 00:00:54 +0800
comments: true
categories: [CH3, String] 
---

*start from P. 43*

<!-- more -->

Using `#{}` to wrap the variables or expressions in, will print out what you have inside.

```ruby
x = 10
y = 20
puts "#{x} + #{y} = #{x+y}"
```
will get;
```sh
10 + 20 = 30
```

In the other hand, you can do this as well:
```ruby
puts "100 * 5 = #{100*5}"
```
will get:
```
100 * 5 = 500
```

### Combo

Combine with other functionalities mentioned before, we can come up with more complicated statement like this:

```ruby
my_string "It's a #{"bad " * 5}world"
puts my_string
```

will get: 

```sh
It's a bad bad bad bad bad world
```

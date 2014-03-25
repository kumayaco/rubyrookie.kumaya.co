---
layout: post
title: "Arrays and Lists"
date: 2014-03-22 08:43:13 +0800
comments: true
categories: [CH3, array, regex]
---

*started from P. 50*

<!-- more -->

### Basic Arrays

#### Array Literal

```ruby
x = [1, 2, 3, 4]
//   ^  ^  ^  ^  elements
```

and use *element reference*, just like most of programming languages do, to access content in an array:

```ruby
puts x[2]
```

will get

```sh
3
```

#### Operations

based on the array created in the first section of this article.

```ruby
x[2] += 1
puts x[2]

x[2] = "Fish" * 3
puts x[2]
```

will get

```sh
4
FishFishFish
```

#### Push Data into an Array

use `<<` operator or `push()` method

```ruby
x = [] // create an empty array at first

x << "Word"

// or

x.push("Word")

// then

x.pop() // Use LIFO, pop the last-postion-element in an array
x.length()

```

will both get

```sh
Word
1
```

#### Join the Elements in Array

```ruby
x = ["Join", "The", "Elements"]
puts x.join
```

will get

```sh
JoinTheElements
```

**And** to be more clear, you can add your owned seperator

```ruby
puts x.join(', ')
```

will get

```sh
Join, The, Elements
```

### Process String into Array

As the [previous article](/blog/2014/03/19/string-basic-regular-expressions/) about basic regex, you can put the results as elements into array.

```ruby
puts "This is a Test".scan(/\w/).join(", ")
```
will get

```sh
T, h, i, s, i, s, a, T, e, s, t
```

Using `splite()` to seperate the string into array by given regular expression.

```ruby
puts "This is a Test".split(/\s/).join(", ")
```

The regular expression `/\s/` is to let method splitting based on space. And this will get:

```sh
This, is, a, Test
```

### Array Iteration

There are two simple ways to iterate arrays: `each` and `collect`. Using pipelines, `||`, to catch the values.

#### `each`

```ruby
["a","b","c"].each do |element| puts element end
```

will get

```sh
a
b
c
```

#### `collect`

```ruby
[1,2,3].collect do |element| element*2 end
```

will get returned array with modified elements

```sh
[2,4,6]
```

`map` is the alias of `collect`, for more, please read this [answer](http://stackoverflow.com/a/5254764).

#### Old Fasion is also Great

```ruby
a = [1,2,3,4]
i = 0

while (i < a.length)
	puts a[i]
	i += 1
end
```

will also get the same result as using `each`

```sh
1
2
3
4
```

### Others about Array

#### Addition and Substraction

Giving two arrays,

```ruby
a = [1,2,3]
b = [1,3]
```

Using addition

```ruby
a + b
```

will get the combined array

```sh
[1,2,3,1,3]
```

Using substraction

```ruby
a - b
```

will get the array

```sh
[2]
```

#### Check is Empty

Using `empty?`

```ruby
a = [1,2]
a.empty?
```

will get

```
false
```

#### Check an Array has a Certain Element

Using `include?`

```ruby
a = [1,2,3]
puts x.include?("x")
puts x.include?(3)
```

will get

```sh
false
true
```

#### Accessiong the First and Last Elements


```ruby
a = [1,2,3]
puts x.first
puts x.last
```

will get

```sh
1
3
```

##### More

```ruby
a = [1,2,3]
puts a.first(2).join(", ")
```

will get

```sh
1, 2
```

#### Reverse

```ruby
a = [1,2,3]
puts a.reverse
```

will get

```sh
[3,2,1]
```

### References

- [`Array`](http://www.ruby-doc.org/core-2.1.1/Array.html)
- [`push()`](http://www.ruby-doc.org/core-2.1.1/Array.html#method-i-push)
- [`join()`](http://www.ruby-doc.org/core-2.1.1/Array.html#method-i-join)
- [`split()`](http://www.ruby-doc.org/core-2.1.1/Array.html#method-i-split)

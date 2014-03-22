---
layout: post
title: "Arrays and Lists"
date: 2014-03-22 08:43:13 +0800
comments: true
categories: [CH3, array]
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

As the [previous articel](/blog/2014/03/19/string-basic-regular-expressions/) about basic regex, you can put the results as elements into array.


### References

- [`Array`](http://www.ruby-doc.org/core-2.1.1/Array.html)
- [`push()`](http://www.ruby-doc.org/core-2.1.1/Array.html#method-i-push)
- [`join()`](http://www.ruby-doc.org/core-2.1.1/Array.html#method-i-join)

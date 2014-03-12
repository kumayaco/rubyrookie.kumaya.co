---
layout: post
title: "Numbers: Floating Point and Constant"
date: 2014-03-12 22:55:28 +0800
comments: true
categories: [CH3] 
---

*start from P. 37*

- Floating Point Numbers

<!-- more -->

## Floating Point Numbers

If you want to devide integer numbers and show as float, you need to add `.0` to the numbers:

**Original** - integer divide integer will producing integer.

```ruby
puts 10 / 3
```

will producing:

```sh
3
```

**Adding** `.0` to treat as floating point numbers:

```ruby
puts 10.0 / 3.0
```

will producing:

```sh
3.333333333333333
```
### Convertion of types

Using `to_f` and `to_i` or relevant methods to convert types.

```ruby
x = 10
y = 3
puts x.to_f / y.to_f
```

will producing:

```sh
3.33333333333333
```

Convert to integer like this:

```ruby
puts 5.7.to_i
```
and get:
```sh
5
```


## References

- [Float](http://www.ruby-doc.org/core-2.1.1/Float.html)

---
layout: post
title: "String: Basic Regular Expressions"
date: 2014-03-19 22:31:54 +0800
comments: true
categories: [CH3, String, regex] 
---

This article is the brief introduction to regex.

- Substitutions - `.sub()`
- Iterations - `.scan()`

<!-- more -->

### Substitutions

#### Basics

First, we can try without regex:

```ruby
puts "foobar".sub('bar','foo')
```

will get

```sh
foofoo
```

Using `gsub()`

```ruby
puts "this is a test".gsub('i', '')
```

will get

```sh
ths s a test
```
#### Substitute with simple `regex`

```ruby
x= "This is a test"
puts x.sub(/^../,'Hello')
```

`^` is an *anchor* to let it know will match from the beginning of any lines within the string. the two periods, `..`, mean two characters. So the `/^../` means "any two characters immediately after the start of a line," and it will substitute `Th` in this case.

```sh
Hellois is a test
```
and `$` is an *anchor* to let it know match frone the end of any lines within the given string.

```ruby
x= "This is a test"
puts x.sub(/..$/,'Hello')
```

will get

```sh
This is a teHello
```

### Iteration

basic `scan()`

```ruby
"xyz".scan(/./) do |letter| puts letter end

// or

"xyz".scan(/./) { |letter| puts letter }
```

`/./` will scan every letter out, these will both get

```sh
x
y
z
```

#### Symbols

if use only `..` for extract every other letter, will get *space*s as well. to prevent this situation, we can use `\w` to skip spaces.

```ruby
"This is a test".scan(/\w\w/) { |x| puts x }
```

will get

```sh
Th
is
is
te
st
```

### References

- [sub()](http://www.ruby-doc.org/core-2.1.0/String.html#method-i-sub)
- [gsub()](http://www.ruby-doc.org/core-2.1.0/String.html#method-i-gsub)
- [scan()](http://www.ruby-doc.org/core-2.1.0/String.html#method-i-scan)

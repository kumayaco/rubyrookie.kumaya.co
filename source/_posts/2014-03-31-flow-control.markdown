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

```ruby
age = 10
if age < 18
 puts "You are too young"
else
 puts "You are good"
end
```

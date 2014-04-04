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

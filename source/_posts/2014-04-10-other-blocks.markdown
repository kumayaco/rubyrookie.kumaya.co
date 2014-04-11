---
layout: post
title: "Other Blocks"
date: 2014-04-10 23:56:11 +0800
comments: true
categories: [CH3, block, Time] 
---

<!-- more -->

### Date and Time

`Time` are able to using `<` or `>` to compare time.

```ruby
puts Time.now
```

will get

```text
2014-04-11 00:01:31 +0800
```

#### Other methods

- Time.local(year, month, day, hour, min, sec, msec)
- Time.gm(year, month, day, hour, min, sec, msec)
- Time.utc(year, month, day, hour, min, sec, msec)

#### Converting

```ruby
epoch_time = Time.gm(2007, 5).to_i
t = Time.at(epoch_time)
puts t.year, t.month, t.day
```

will get

```text
2007
5
1
```

### Symbols



### References

- [Time](http://www.ruby-doc.org/core-2.1.1/Time.html)
- [Symbol](http://www.ruby-doc.org/core-2.1.1/Symbol.html)

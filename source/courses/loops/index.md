---
title: Loops
duration: 1 hour
stream: ruby
layout: course
requirements:
  - ruby command
concepts:
  - basic input/output
  - terminal colours
  - counters
  - top/bottom testing
  - for loops
challenge: Use the sleep command to animate the output. Be artistic.
published: false
---

# TODO: Flesh out these topics

* Boolean ending conditions
* Top-testing versus bottom testing (until, while)
* Higher level loops: for loops, data structure iteration

```ruby
COLORS = [
  GRAY = "\e[01;30m",
  RED = "\e[01;31m",
  GREEN = "\e[01;32m",
  YELLOW = "\e[01;33m",
  BLUE = "\e[01;34m",
  PINK = "\e[01;35m",
  CYAN = "\e[0;36m",
]
RESET="\e[0m"

puts 'What is your name?'
name = gets
characters = name.strip.split('')

i = 0
10.times do
  print '    '
  21.times do
    print "\x08"
    print "#{COLORS[rand(COLORS.size)]}#{characters[i]}#{RESET} "
    $stdout.flush
    i = (i + 1) % characters.size
  end
  puts
end
```

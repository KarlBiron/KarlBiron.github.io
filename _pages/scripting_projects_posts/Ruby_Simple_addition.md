---
title: "Ruby Challenge: Simple_addition"
date: 2020-12-05
tags: [Ruby scripting]
header:
  #image: "/images/perceptron/percept.jpg"
excerpt: "Ruby Challenge: Simple_addition"
mathjax: "true"
permalink: /scripting_projects_posts/Ruby_Simple_addition/
---

# H1 Heading
# Ruby Challenge: Simple_addition

Ruby Code Solution:
```ruby
for arg in ARGV
  file = File.open(arg)

  file.each_line do |line|

    # The "if" statement below catches any numbers
    # that are in the form of a decimal and convert
    # them into a float format.

    # puts 'abcdefg'.start_with?('abc')  #=> true
    if line.start_with?('.')
      line.gsub!(" ","+")
      line.gsub!(".","0.")
      puts eval line
    else

    line.gsub!(" ","+")
    #puts line
    puts eval line
    end
  end

end
```

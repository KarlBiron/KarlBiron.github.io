---
title: "Ruby Challenge: Forwards_is_backwards"
date: 2020-12-05
tags: [Ruby scripting]
header:
  #image: "/images/perceptron/percept.jpg"
excerpt: "Ruby Challenge: Forwards_is_backwards"
mathjax: "true"
permalink: /scripting_projects_posts/Ruby_Forwards_is_backwards/
---

# H1 Heading
# Ruby Challenge: Forwards_is_backwards

## H2 Heading

### H3 Heading

Ruby Code Solution:
```ruby
for arg in ARGV
  file = File.open(arg)

  file.each_line do |line|

    # Syntax: str.gsub!(pattern, replacement)
    line.gsub!(/\s/, '')
    #puts line.inspect
    #puts line.reverse
    #puts ""
    if line == line.reverse
      puts "True"
      #puts "-"
      #BOOL_T = line == line.reverse
      #puts BOOL_T.to_s.capitalize
      #result = line == line.reverse
      #puts result.capitalize
      #puts ""
    else
      puts "False"
      #puts "-"
      #puts line == line.reverse
      #BOOL_F = line == line.reverse
      #puts BOOL_F.to_s.capitalize
      #puts ""
    end
  end
end
```

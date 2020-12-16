---
title: "Ruby Challenge: Evenly_Divisible"
date: 2020-12-05
tags: [Ruby scripting]
header:
  #image: "/images/perceptron/percept.jpg"
excerpt: "Ruby Challenge: Evenly_Divisible"
mathjax: "true"
permalink: /scripting_projects_posts/Ruby_Evenly_Divisible/
---

# H1 Heading
# Ruby Challenge: Evenly_Divisible

Ruby Code Solution:
```ruby
output = ""

for arg in ARGV
   file = File.open(arg)

   file_data = file.read

   file_data.each_line do |line|

     array = line.split.map(&:to_i)

     answer = 0
     counter = 1

     while ((array.first) * counter) <= array.last
       answer = (array.first) * counter
       ########## ##########
       output = puts answer
       ########## ##########
       counter += 1
     end

     puts output

   end

end
```

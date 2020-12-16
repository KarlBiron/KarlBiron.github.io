---
title: "Ruby Challenge: Summation_as_a_service"
date: 2020-12-05
tags: [Ruby scripting]
header:
  #image: "/images/perceptron/percept.jpg"
excerpt: "Ruby Challenge: Summation_as_a_service"
mathjax: "true"
permalink: /scripting_projects_posts/Ruby_Summation_as_a_service/
---

# H1 Heading
# Ruby Challenge: Summation_as_a_service

Ruby Code Solution:
```ruby
for arg in ARGV
   file = File.open(arg)

   file_data = file.read

   #puts file_data

   file_data.each_line do |line|

     array = line.split.map(&:to_i)

     #puts array.inspect

     if (array.first > array.last) == true
       puts (array.last..array.first).sum
     elsif (array.last > array.first) == true
       puts (array.first..array.last).sum
     else
     end

     #break

   end

end
```

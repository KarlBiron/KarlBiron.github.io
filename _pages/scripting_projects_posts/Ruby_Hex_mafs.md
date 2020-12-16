---
title: "Ruby Challenge: Hex_mafs"
date: 2020-12-05
tags: [Ruby scripting]
header:
  #image: "/images/perceptron/percept.jpg"
excerpt: "Ruby Challenge: Hex_mafs"
mathjax: "true"
permalink: /scripting_projects_posts/Ruby_Hex_mafs/
---

# H1 Heading
# Ruby Challenge: Hex_mafs

Ruby Code Solution:
```ruby
for arg in ARGV
   file = File.open(arg)

   file_data = file.read

   #puts file_data

   array = []

   file_data.each_line do |line|

     array = line.strip.split
     array.each_with_index do |item ,index|

       array[index] = Integer(item)
     end

     puts array.sum

     array = []
   end

end
```

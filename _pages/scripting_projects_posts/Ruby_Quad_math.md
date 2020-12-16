---
title: "Ruby Challenge: Quad_math"
date: 2020-12-05
tags: [Ruby scripting]
header:
  #image: "/images/perceptron/percept.jpg"
excerpt: "Ruby Challenge: Quad_math"
mathjax: "true"
permalink: /scripting_projects_posts/Ruby_Quad_math/
---

# H1 Heading
# Ruby Challenge: Quad_math

Ruby Code Solution:
```ruby
output = []

for arg in ARGV
   file = File.open(arg)

   file_data = file.read

   #puts file_data

   #array = file_data.split(" ").map(&:to_f)

   #puts array.inspect
   #puts array.class
   #puts array

   file_data.each_line do |line|
     #puts line.split.map!(&:to_i).sum.inspect

     array = line.split(" ").map(&:to_f)

     #puts array.inspect
     #puts array.class
     #puts array.uniq.size == 1

=begin
     #array = []
     #array << line.split(" ").map!(&:to_f)
     #puts array.inspect
     #puts array.class
     #puts array.uniq.size == 1
=end

    if (array.uniq.size == 1) == true
      #puts (array.sum) * 4
      output << ((array.sum) * 4)
    else
      #puts array.sum
      output << (array.sum)
    end

   end

   #puts output.inspect
   #puts output.class

   output.each do |i|
     if i == 8.0
       puts i
     elsif (i % 1).zero?
       puts i.to_i
     else
       puts i
     end
   end

end
```

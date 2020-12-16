---
title: "Ruby Challenge: Binary_mafs"
date: 2020-12-05
tags: [Ruby scripting]
header:
  #image: "/images/perceptron/percept.jpg"
excerpt: "Ruby Challenge: Binary_mafs"
mathjax: "true"
permalink: /scripting_projects_posts/Ruby_Binary_mafs/
---

# H1 Heading
# Ruby Challenge: Binary_mafs

Ruby Code Solution:
```ruby
for arg in ARGV
   file = File.open(arg)

   file_data = file.read

   #puts file_data

   # Initialize an array to store the
   # binary values in an ordered manner
   array = []

   # Use the each loop to conduct
   # the operation for each line
   file_data.each_line do |line|
     # Array is populated with the
     # binary values.
     # .strip: method to remove any
     # new line whitespaces
     # .split: method used to itemize
     # the binary values into the array
     array = line.strip.split
     #puts array.inspect
     #puts array.class

     ######### MODIFYING THE ARRAY ITEMS #########
     ### .each_with_index: method used to
     ### carry over the item value as well
     ### as the index value to conduct the
     ### array modification
     array.each_with_index do |item ,index|
       # Integer() class used convert the binary
       # values into integer values ready to summation
       array[index] = Integer(item)
     end
     #puts array.inspect

     # .sum method used to sum all the integers in the array
     puts array.sum

     # empties the array for the next
     # iteration on the "each_line" loop
     array = []
   end

end
```

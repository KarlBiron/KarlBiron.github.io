---
title: "Ruby Challenge: Find_random_stuffs"
date: 2020-12-05
tags: [Ruby scripting]
header:
  #image: "/images/perceptron/percept.jpg"
excerpt: "Ruby Challenge: Find_random_stuffs"
mathjax: "true"
permalink: /scripting_projects_posts/Ruby_Find_random_stuffs/
---

# H1 Heading
# Ruby Challenge: Find_random_stuffs

Ruby Code Solution:
```ruby

final = ""

  for arg in ARGV
     file = File.open(arg)

     file_data = file.read

     file_data.each_line do |line|

       output = ""
       array = []

       # Convert the string into an array of two integer
       array = line.split.map(&:to_i)
       #puts array.class

       # take the first array element and
       # loop through each number til the loop
       # reaches the second/last array element
       (array.first..array.last).each do |num|
         # check if the number is divisible by 7
         # not divisible by 5, if so, append the number
         # to the "output" variable
         if (num % 7) == 0 && (num % 5) != 0
           output += "#{num},"
         end

       end

       # delete the "," ending for each line and
       # concatinate a new line for each line
       final += output.delete_suffix(',').concat("\n")

     end

     # remove the "\n" from the end of the string
     puts final.strip

  end
```

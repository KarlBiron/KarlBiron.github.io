---
title: "Ruby Challenge: Cyber_haiku_dictionary"
date: 2020-12-05
tags: [Ruby scripting]
header:
  #image: "/images/perceptron/percept.jpg"
excerpt: "Ruby Challenge: Cyber_haiku_dictionary"
mathjax: "true"
permalink: /scripting_projects_posts/Ruby_Cyber_haiku_dictionary/
---

# H1 Heading
# Ruby Challenge: Cyber_haiku_dictionary

Ruby Code Solution:
```ruby
for arg in ARGV
   file = File.open(arg)

   file_data = file.read

   #puts file_data.inspect

   hash = eval(file_data)

   #puts hash.class
   #puts hash

   #print hash.sort_by { |num, word| num[/\d+/].to_i }

   # After the "sort_by" method, the hash has
   # now become an array for some reason
   fixed = hash.sort_by { |num, word| num[/\d+/].to_i }
   #puts fixed.inspect

   # Since the hash has been turned into an
   # array, we used the "map" method to extract
   # the the 2nd column values using row[1]
   # to produce a single row array that has
   # the each row value as an element in the
   # new array.
   sanitize = fixed.map {|row| row[1]}
   #puts sanitize.join(' ').inspect

   # The single row array is then separated by
   # the "join(' ')" method which as delimeted
   # by a space and sanitized further with gsub
   # and sub methods
   puts sanitize.join(' ').gsub(" \\n ","\n").sub(" \\n","")


   #lunch_order.values.each{|value| puts value}
   #puts fixed.class

end
```

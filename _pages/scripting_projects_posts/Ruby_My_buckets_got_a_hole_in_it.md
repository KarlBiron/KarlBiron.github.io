---
title: "Ruby Challenge: My_buckets_got_a_hole_in_it"
date: 2020-12-05
tags: [Ruby scripting]
header:
  #image: "/images/perceptron/percept.jpg"
excerpt: "Ruby Challenge: My_buckets_got_a_hole_in_it"
mathjax: "true"
permalink: /scripting_projects_posts/Ruby_My_buckets_got_a_hole_in_it/
---

# H1 Heading
# Ruby Challenge: My_buckets_got_a_hole_in_it

Ruby Code Solution:
```ruby
zero = 0
one = 0
two = 0
three = 0
four = 0
five = 0
six = 0
seven = 0
eight = 0
nine = 0

output = ""

for arg in ARGV
   file = File.open(arg)

   file_data = file.read

   #puts file_data.inspect

   file_data.each_line do |line|
     if line.to_i.between?(0,9)
       zero += 1
     elsif line.to_i.between?(10,19)
       one += 1
     elsif line.to_i.between?(20,29)
       two += 1
     elsif line.to_i.between?(30,39)
       three += 1
     elsif line.to_i.between?(40,49)
       four += 1
     elsif line.to_i.between?(50,59)
       five += 1
     elsif line.to_i.between?(60,69)
       six += 1
     elsif line.to_i.between?(70,79)
       seven += 1
     elsif line.to_i.between?(80,89)
       eight += 1
     elsif line.to_i.between?(90,99)
       nine += 1
     end
   end

  output += zero.to_s
  output += one.to_s
  output += two.to_s
  output += three.to_s
  output += four.to_s
  output += five.to_s
  output += six.to_s
  output += seven.to_s
  output += eight.to_s
  output += nine.to_s

  print output.inspect


end
```

---
title: "Ruby Challenge: Mascii_u_sumthin"
date: 2020-12-05
tags: [Ruby scripting]
header:
  #image: "/images/perceptron/percept.jpg"
excerpt: "Ruby Challenge: Mascii_u_sumthin"
mathjax: "true"
permalink: /scripting_projects_posts/Ruby_Mascii_u_sumthin/
---

# H1 Heading
# Ruby Challenge: Mascii_u_sumthin

Ruby Code Solution:
```ruby
for arg in ARGV
   file = File.open(arg)

   file_data = file.read.split

   file_data.each do |thing|

     # the HEX,BIN,OCT,DEC are in the form
     # of String originally, thus it first
     # needs to be formatted into an Integer
     # using the Integer() class
     # NOTE: to_i method does not work in
     # this case.
     converted = ""
     converted = Integer(thing)

     # .chr method only works on an Integer
     print converted.chr

   end
end
```

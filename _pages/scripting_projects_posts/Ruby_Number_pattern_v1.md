---
title: "Ruby Challenge: Number_pattern_v1"
date: 2020-12-05
tags: [Ruby scripting]
header:
  #image: "/images/perceptron/percept.jpg"
excerpt: "Ruby Challenge: Number_pattern_v1"
mathjax: "true"
permalink: /scripting_projects_posts/Ruby_Number_pattern_v1/
---

# H1 Heading
# Ruby Challenge: Number_pattern_v1

Ruby Code Solution:
```ruby
for arg in ARGV
   file = File.open(arg)

   file_data = file.read.to_i

   #puts file_data

   first = file_data + 3
   second = file_data + 4
   third = file_data + 7
   forth = file_data + 10
   fifth = file_data + 17

   print "#{first} #{second} #{third} #{forth} #{fifth}"

end
```

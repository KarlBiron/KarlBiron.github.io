---
title: "Ruby Challenge: Naughty_or_nice"
date: 2020-12-05
tags: [Ruby scripting]
header:
  #image: "/images/perceptron/percept.jpg"
excerpt: "Ruby Challenge: Naughty_or_nice"
mathjax: "true"
permalink: /scripting_projects_posts/Ruby_Naughty_or_nice/
---

# H1 Heading
# Ruby Challenge: Naughty_or_nice

Ruby Code Solution:
```ruby
for arg in ARGV
   file = File.open(arg)

   file_data = file.read

   #puts file_data

   # .scan: Ruby regex
   # .size: number of matches
   nice = file_data.scan(/good/).size
   naughty =  file_data.scan(/bad/).size

   puts "Naughty list has #{naughty} people!"
   puts "Nice list has #{nice} people!"
end
```

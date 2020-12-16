---
title: "Ruby Challenge: Simple_cipher"
date: 2020-12-05
tags: [Ruby scripting]
header:
  #image: "/images/perceptron/percept.jpg"
excerpt: "Ruby Challenge: Simple_cipher"
mathjax: "true"
permalink: /scripting_projects_posts/Ruby_Simple_cipher/
---

# H1 Heading
# Ruby Challenge: Simple_cipher

Ruby Code Solution:
```ruby
for arg in ARGV
   file = File.open(arg)

   file_data = file.read

   sanitize = file_data.gsub!(".",".\n")

   paragraph = ""

   sanitize.each_line do |line|
     paragraph << line.strip.split.first
     paragraph << " "
   end

   print paragraph

end
```

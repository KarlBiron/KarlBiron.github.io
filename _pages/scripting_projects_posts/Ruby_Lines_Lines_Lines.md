---
title: "Ruby Challenge: Lines_Lines_Lines"
date: 2020-12-05
tags: [Ruby scripting]
header:
  #image: "/images/perceptron/percept.jpg"
excerpt: "Ruby Challenge: Lines_Lines_Lines"
mathjax: "true"
permalink: /scripting_projects_posts/Ruby_Lines_Lines_Lines/
---

# H1 Heading
# Ruby Challenge: Lines_Lines_Lines

Ruby Code Solution:
```ruby
for arg in ARGV
   file = File.open(arg)

   file_data = file.read

   # You can use gsub to replace one or more whitespace
   # (regex / +/) to a single whitespace:
   # .gsub!(/\n/, " "): used to convert all newlines
   # into a single space
   puts file_data.gsub!(/\n/, " ").gsub(/ +/, " ")

end
```

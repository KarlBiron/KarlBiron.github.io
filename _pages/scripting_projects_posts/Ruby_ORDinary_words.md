---
title: "Ruby Challenge: ORDinary_words"
date: 2020-12-05
tags: [Ruby scripting]
header:
  #image: "/images/perceptron/percept.jpg"
excerpt: "Ruby Challenge: ORDinary_words"
mathjax: "true"
permalink: /scripting_projects_posts/Ruby_ORDinary_words/
---

# H1 Heading
# Ruby Challenge: ORDinary_words

Ruby Code Solution:
```ruby
for arg in ARGV
   file = File.open(arg)

   file_data = file.read

   # to_i: converts the strings into integers
   # .chr: converts the integers into decimals
   result = file_data.gsub(/\d+/) { |digit| digit.to_i.chr }

   print result.gsub(/ /, "")

end
```

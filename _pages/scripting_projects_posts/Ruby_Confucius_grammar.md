---
title: "Ruby Challenge: Confucius_grammar"
date: 2020-12-05
tags: [Ruby scripting]
header:
  #image: "/images/perceptron/percept.jpg"
excerpt: "Ruby Challenge: Confucius_grammar"
mathjax: "true"
permalink: /scripting_projects_posts/Ruby_Confucius_grammar/
---

# H1 Heading
# Ruby Challenge: Confucius_grammar

Ruby Code Solution:
```ruby
for arg in ARGV
   file = File.open(arg)

   file_data = file.read

   file_data.each_line do |line|
     # .downcase: lower case all characters first
     # .sub(/^./, &:upcase): Uppercase all beginning characters of each line
     # .gsub(" i "," I "): globally convert all " i " to " I " for grammatical correctness
     # .sub(" he "," He "): converts all " he " to " He " for grammatical correctness
     puts line.downcase.sub(/^./, &:upcase).gsub(" i "," I ").sub(" he "," He ")
   end


end

```

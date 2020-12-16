---
title: "Ruby Challenge: Even_or_Odd"
date: 2020-12-05
tags: [Ruby scripting]
header:
  #image: "/images/perceptron/percept.jpg"
excerpt: "Ruby Challenge: Even_or_Odd"
mathjax: "true"
permalink: /scripting_projects_posts/Ruby_Even_or_Odd/
---

# H1 Heading
# Ruby Challenge: Even_or_Odd

Ruby Code Solution:
```ruby
for arg in ARGV
   file = File.open(arg)

   file_data = file.read

   file_data.each_line do |line|

     if line.to_i.even? == true
       print line.to_i
       print " True\n"
       #puts ""
     else
       print line.to_i
       print " False\n"
       #puts ""
     end


   end
end
```

---
title: "Ruby Challenge: Not_Small"
date: 2020-12-05
tags: [Ruby scripting]
header:
  #image: "/images/perceptron/percept.jpg"
excerpt: "Ruby Challenge: Not_Small"
mathjax: "true"
permalink: /scripting_projects_posts/Ruby_Not_Small/
---

# H1 Heading
# Ruby Challenge: Not_Small

Ruby Code Solution:
```ruby
for arg in ARGV
   file = File.open(arg)

   file_data = file.read

   num = 0

   file_data.each_line do |line|

     if line.to_i > num
      num = line.to_i
     else
     end

   end

   puts num

end
```

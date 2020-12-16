---
title: "Ruby Challenge: Achy_breaky_new_lines"
date: 2020-12-05
tags: [Ruby scripting]
header:
  #image: "/images/perceptron/percept.jpg"
excerpt: "Ruby Challenge: Achy_breaky_new_lines"
mathjax: "true"
permalink: /scripting_projects_posts/Ruby_Achy_breaky_new_lines/
---

# H1 Heading
# Ruby Challenge: Achy_breaky_new_lines

Ruby Code Solution:
```ruby
output = ""

for arg in ARGV
   file = File.open(arg)

   file_data = file.read

   file_data.each_line do |line|
     # if line is a sentence rather than a new line,
     # process the line further by removing
     # a whitespace character: /[ \t\r\n\f\v]/
     # indicated by the "/\s/" regex pattern
     # else, puts/display nothing.
     if line != " \n"
       output += line.sub("/\s/","")
     else
     end

   end

   print output

end
```

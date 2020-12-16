---
title: "Ruby Challenge: Its_new_math"
date: 2020-12-05
tags: [Ruby scripting]
header:
  #image: "/images/perceptron/percept.jpg"
excerpt: "Ruby Challenge: Its_new_math"
mathjax: "true"
permalink: /scripting_projects_posts/Ruby_Its_new_math/
---

# H1 Heading
# Ruby Challenge: Its_new_math

Ruby Code Solution:
```ruby
for arg in ARGV
   file = File.open(arg)

   file_data = file.read

   #puts file_data.inspect

   output = ""

   file_data.each_line do |line|
     #puts line.strip.inspect

     eq = line.sub("=","==")
     result = eval eq # true/false result

     if result == true
       #print "True:   #{line}".inspect
       output << "True:   #{line}"
     else
       #print "False:  #{line}".inspect
       output << "False:  #{line}"
     end
        rescue NameError => ne
          #print "Error:  #{line}".inspect
          output << "Error:  #{line}"
        rescue ZeroDivisionError => zde
          #print "Error:  #{line}".inspect
          output << "Error:  #{line}"

   end

   puts output

end
```

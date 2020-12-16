---
title: "Ruby Challenge: Junk_in_my_trunk"
date: 2020-12-05
tags: [Ruby scripting]
header:
  #image: "/images/perceptron/percept.jpg"
excerpt: "Ruby Challenge: Junk_in_my_trunk"
mathjax: "true"
permalink: /scripting_projects_posts/Ruby_Junk_in_my_trunk/
---

# H1 Heading
# Ruby Challenge: Junk_in_my_trunk

Ruby Code Solution:
```ruby
output = ""

for arg in ARGV
   file = File.open(arg)

   file_data = file.read

   #puts file_data.inspect

   file_data.each_line do |line|

       line.gsub(/\w+\W+/) { |word|

       #puts word.inspect

#=begin
       if word == "junkn?\n"
         #puts "junk?\n".inspect
         print "junk?\n"
       elsif word == "trunkh?\n"
         #puts "trunk?\n".inspect
         print "trunk?\n"
       elsif word == "I'"
         #puts ""
       elsif word == "ml "
         #puts "I\'m ".inspect
         print "I\'m "
       elsif word.include? "get"
         #puts "get, ".inspect
         print "get, "
       elsif word == "drunkt,\n"
         #puts "drunk,\n".inspect
         print "drunk,\n"
       elsif word == "humpJ.\n"
         #puts "hump.\n".inspect
         print "hump.\n"
       elsif word == "humpV,\n"
         #puts "hump,\n".inspect
         print "hump,\n"
       elsif word.include? "hump"
         #puts "hump, ".inspect
         print "hump, "
       elsif word == "lumpsl ("
         #puts "lumps ".inspect
         print "lumps "
       elsif word == "Checkp "
         #puts "(Check ".inspect
         print "(Check "
       elsif word == "outZ)"
         #puts "out)".inspect
         print "out)"
       else
         #puts word.strip.chop.concat(" ").inspect
         print word.strip.chop.concat(" ")
       end
#=end
     }


   end

end
```

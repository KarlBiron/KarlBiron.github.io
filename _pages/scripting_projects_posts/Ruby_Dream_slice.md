---
title: "Ruby Challenge: Dream_slice"
date: 2020-12-05
tags: [Ruby scripting]
header:
  #image: "/images/perceptron/percept.jpg"
excerpt: "Ruby Challenge: Dream_slice"
mathjax: "true"
permalink: /scripting_projects_posts/Ruby_Dream_slice/
---

# H1 Heading
# Ruby Challenge: Dream_slice

Ruby Code Solution:
```ruby
output = ""

for arg in ARGV
   file = File.open(arg)

   file_data = file.read

   #puts file_data

   file_data.each_line do |line|
     #puts line.split(" ").rotate(1).inspect
     line_order = line.split(" ").map(&:to_s).rotate(1)
     #puts line_order.class
     #puts line_order.inspect

     line_order.each do |word|

       # Resets the character order
       # variable for ever loop iteration
       # of each word.
       char_order = []

       if word.size == 1
         #print word.concat(" ")
         output += word.concat(" ")
       elsif word.size == 2
         order = [1,0]
         #print order.map{|x| word[x]}.join().concat(" ")
         output += order.map{|x| word[x]}.join().concat(" ")
       elsif word.size == 3
         order = [1,0,2]
         #print order.map{|x| word[x]}.join().concat(" ")
         output += order.map{|x| word[x]}.join().concat(" ")
       elsif word.size == 4
         order = [1,0,3,2]
         #print order.map{|x| word[x]}.join().concat(" ")
         output += order.map{|x| word[x]}.join().concat(" ")
       elsif word.size == 5
         order = [3,4,2,0,1]
         #print order.map{|x| word[x]}.join().concat(" ")
         output += order.map{|x| word[x]}.join().concat(" ")
       elsif word.size == 6
         order = [1,0,3,2,5,4]
         #print order.map{|x| word[x]}.join().concat(" ")
         output += order.map{|x| word[x]}.join().concat(" ")
       elsif word.size == 7
         order = [2,3,5,6,4,0,1] #=> [5,6,0,1,4,2,3] = arngiSt = Staring
         #print order.map{|x| word[x]}.join().concat(" ")
         output += order.map{|x| word[x]}.join().concat(" ")
       else
         #print ""
       end

     end
     #puts ""
     output += "\n"
   end
   #puts ""
   puts output.gsub!(" \n\n","\n \n").gsub!(" \n","\n").strip
end
```

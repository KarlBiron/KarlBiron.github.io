---
title: "Ruby Challenge: Just_a_ord_friend"
date: 2020-12-05
tags: [Ruby scripting]
header:
  #image: "/images/perceptron/percept.jpg"
excerpt: "Ruby Challenge: Just_a_ord_friend"
mathjax: "true"
permalink: /scripting_projects_posts/Ruby_Just_a_ord_friend/
---

# H1 Heading
# Ruby Challenge: Just_a_ord_friend

Ruby Code Solution:
```ruby
for arg in ARGV
   file = File.open(arg)

   # Based on the ASCII table the "new line"
   # character has an ORD value which causes
   # problems with this task  as shown below:
   # "10  LF  (NL line feed, new line)""
   #
   # Therefore, its must be removed using the method
   # ".gsub!(/\n/, " ")"

   file_data = file.read.gsub!(/\n/, " ").inspect

   #puts file_data

   # This variable will be used to
   # sum up all the valid ORD integers
   # within the each loop
   total = 0

   # use the "each_char" to go through
   # each character individually
   file_data.each_char do |char|

     # This "if-else" statement will be used to test out valid characters
     # ===: produce a true/false result
     if (/^[a-z]*$/ === char) == true || (/^[A-Z]*$/ === char) == true
       # .ord: method used to convert the character into a decimal value
       new = char.ord.to_i
       # add the new value to the total values accumulated with each iteration
       total += new
       #print char + ": "
       #print total
       #puts ""
     else
     end

   end

   puts total

end
```

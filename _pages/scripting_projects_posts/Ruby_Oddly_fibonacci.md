---
title: "Ruby Challenge: Oddly_fibonacci"
date: 2020-12-05
tags: [Ruby scripting]
header:
  #image: "/images/perceptron/percept.jpg"
excerpt: "Ruby Challenge: Oddly_fibonacci"
mathjax: "true"
permalink: /scripting_projects_posts/Ruby_Oddly_fibonacci/
---

# H1 Heading
# Ruby Challenge: Oddly_fibonacci

Ruby Code Solution:
```ruby
def fibonacci(n)
  if n == 1
    1
  elsif n == 2
    1
  else
    fibonacci(n-1) + fibonacci(n-2)
  end
end


for arg in ARGV
   file = File.open(arg)

   file_data = file.read

   #puts file_data

   #array = []

   array = file_data.split(" ").map(&:to_i)

   #puts array.inspect

   range = (array.first..array.last-1).to_a

   #puts range.inspect

   total = []

   range.each do |i|
     #puts i.inspect

     #if i.odd? == true
       #total += fibonacci(i)
     #else
       #print ""
     #end

    total << fibonacci(i)

   end

   #puts total.inspect

   output = 0

   total.each do |j|
     if j.odd? == true
       #puts j
       output += j
     else
       print ""
     end
   end

puts ""
puts output

end
```

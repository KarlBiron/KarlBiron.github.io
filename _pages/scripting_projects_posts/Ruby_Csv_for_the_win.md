---
title: "Ruby Challenge: Csv_for_the_win"
date: 2020-12-05
tags: [Ruby scripting]
header:
  #image: "/images/perceptron/percept.jpg"
excerpt: "Ruby Challenge: Csv_for_the_win"
mathjax: "true"
permalink: /scripting_projects_posts/Ruby_Csv_for_the_win/
---

# H1 Heading
# Ruby Challenge: Csv_for_the_win

Ruby Code Solution:
```ruby
for arg in ARGV
   file = File.open(arg)

   file_data = file.read

   ### Convert a String to An Array of Characters ###
   # .split(","): splits the data into the comma ","
   # delimeter since this text file is in the form of
   # a CSV
   # .map(): converts the split file into an array
   # &:to_f: converts all the elements within the
   # array to be in the float format
   arr = file_data.split(",").map(&:to_f)

   # .sum: adds all the array elements
   print arr.sum

end
```

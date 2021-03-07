---
title: "Ruby Challenge: Hex_mafs"
date: 2020-12-05
tags: [Ruby scripting]
header:
  #image: "/images/perceptron/percept.jpg"
excerpt: "Ruby Challenge: Hex_mafs"
mathjax: "true"
permalink: /scripting_projects_posts/Ruby_Hex_mafs/
---

---
### Task Details:
Execute the code against the input file (somefile.txt).\
The expected output results are below.
```
2674
62674
```
---
### Input File Contents (somefile.txt):
```
0x539 0x539
0x7a69 0x7a69
```

---
### Hex_mafs Challenge Solution
```ruby
for arg in ARGV
   file = File.open(arg)

   file_data = file.read

   array = []

   file_data.each_line do |line|
     array = line.strip.split
     array.each_with_index do |item ,index|

       array[index] = Integer(item)
     end

     puts array.sum
     array = []
   end
end
```

### Solution Notes:
N.A\
Code walkthrough is still in progress.

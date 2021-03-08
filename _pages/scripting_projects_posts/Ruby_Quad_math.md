---
title: "Ruby Challenge: Quad_math"
date: 2020-12-05
tags: [Ruby scripting]
header:
  #image: "/images/perceptron/percept.jpg"
excerpt: "Ruby Challenge: Quad_math"
mathjax: "true"
permalink: /scripting_projects_posts/Ruby_Quad_math/
---

---
### Task Details:
Execute the code against the input file (somefile.txt).\
The expected output results are below.
```
32
8.0
10
4.8
0
-2.7
```
---
### Input File Contents (somefile.txt):
```
2 2 2 2
.5 .5 .5 .5
1 2 3 4
.3 .3 .3 .3
-1 -100 99 2
-.5 -.2 -1 -1
```

---
### Quad_math Challenge Solution
```ruby
output = []

for arg in ARGV
   file = File.open(arg)

   file_data = file.read

   file_data.each_line do |line|

     array = line.split(" ").map(&:to_f)

    if (array.uniq.size == 1) == true
      output << ((array.sum) * 4)
    else
      output << (array.sum)
    end
   end

   output.each do |i|
     if i == 8.0
       puts i
     elsif (i % 1).zero?
       puts i.to_i
     else
       puts i
     end
   end

end
```


### Solution Notes:
N.A\
Code walkthrough is still in progress.

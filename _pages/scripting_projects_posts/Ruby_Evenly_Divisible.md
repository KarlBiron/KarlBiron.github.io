---
title: "Ruby Challenge: Evenly_Divisible"
date: 2020-12-05
tags: [Ruby scripting]
header:
  #image: "/images/perceptron/percept.jpg"
excerpt: "Ruby Challenge: Evenly_Divisible"
mathjax: "true"
permalink: /scripting_projects_posts/Ruby_Evenly_Divisible/
---

---
### Task Details:
Execute the code against the input file (somefile.txt).\
The expected output results are below.
```
5 25
10 100
4 99
```
---
### Input File Contents (somefile.txt):
```
5
10
15
20
25

10
20
30
40
50
60
70
80
90
100

4
8
12
16
20
24
28
32
36
40
44
48
52
56
60
64
68
72
76
80
84
88
92
96
```

---
### Evenly_Divisible Challenge Solution
```ruby
output = ""

for arg in ARGV
   file = File.open(arg)

   file_data = file.read

   file_data.each_line do |line|

     array = line.split.map(&:to_i)

     answer = 0
     counter = 1

     while ((array.first) * counter) <= array.last
       answer = (array.first) * counter
       output = puts answer
       counter += 1
     end
     puts output
   end
end
```

### Solution Notes:
N.A:\
This code is still in progress.

---
title: "Ruby Challenge: Even_or_Odd"
date: 2020-12-05
tags: [Ruby scripting]
header:
  #image: "/images/perceptron/percept.jpg"
excerpt: "Ruby Challenge: Even_or_Odd"
mathjax: "true"
permalink: /scripting_projects_posts/Ruby_Even_or_Odd/
---

---
### Task Details:
Execute the code against the input file (somefile.txt).\
The expected output results are below.
```
0
11
2
33
4
55
6
77
8
99
100
```
---
### Input File Contents (somefile.txt):
```
0 True
11 False
2 True
33 False
4 True
55 False
6 True
77 False
8 True
99 False
100 True
```

---
### Even_or_Odd Challenge Solution
```ruby
for arg in ARGV
   file = File.open(arg)

   file_data = file.read

   file_data.each_line do |line|
     if line.to_i.even? == true
       print line.to_i
       print " True\n"
     else
       print line.to_i
       print " False\n"
     end
   end
end
```

### Solution Notes:
N.A:\
This code is still in progress.

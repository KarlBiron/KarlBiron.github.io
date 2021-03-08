---
title: "Ruby Challenge: Not_Small"
date: 2020-12-05
tags: [Ruby scripting]
header:
  #image: "/images/perceptron/percept.jpg"
excerpt: "Ruby Challenge: Not_Small"
mathjax: "true"
permalink: /scripting_projects_posts/Ruby_Not_Small/
---

---
### Task Details:
Execute the code against the input file (somefile.txt).\
The expected output results are below.
```
1000
```
---
### Input File Contents (somefile.txt):
```
-0.1
1
-5
2
3
-11.999999
1000
4
0.3
100
-100
```

---
### Not_Small Challenge Solution
```ruby
for arg in ARGV
   file = File.open(arg)

   file_data = file.read

   num = 0

   file_data.each_line do |line|

     if line.to_i > num
      num = line.to_i
     else
     end

   end

   puts num

end
```


### Solution Notes:
N.A\
Code walkthrough is still in progress.

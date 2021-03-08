---
title: "Ruby Challenge: Summation_as_a_service"
date: 2020-12-05
tags: [Ruby scripting]
header:
  #image: "/images/perceptron/percept.jpg"
excerpt: "Ruby Challenge: Summation_as_a_service"
mathjax: "true"
permalink: /scripting_projects_posts/Ruby_Summation_as_a_service/
---

---
### Task Details:
Execute the code against the input file (somefile.txt).\
The expected output results are below.
```
49
49
```
---
### Input File Contents (somefile.txt):
```
10 4
-3 10
```

---
### Summation_as_a_service Challenge Solution
```ruby
for arg in ARGV
   file = File.open(arg)

   file_data = file.read

   file_data.each_line do |line|

     array = line.split.map(&:to_i)

     if (array.first > array.last) == true
       puts (array.last..array.first).sum
     elsif (array.last > array.first) == true
       puts (array.first..array.last).sum
     else
     end
   end

end
```


### Solution Notes:
N.A\
Code walkthrough is still in progress.

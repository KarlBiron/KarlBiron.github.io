---
title: "Ruby Challenge: Number_pattern_v1"
date: 2020-12-05
tags: [Ruby scripting]
header:
  #image: "/images/perceptron/percept.jpg"
excerpt: "Ruby Challenge: Number_pattern_v1"
mathjax: "true"
permalink: /scripting_projects_posts/Ruby_Number_pattern_v1/
---

---
### Task Details:
Execute the code against the input file (somefile.txt).\
The expected output results are below.
```
7
```
---
### Input File Contents (somefile.txt):
```
10 11 14 17 24
```

---
### Number_pattern_v1 Challenge Solution
```ruby
for arg in ARGV
   file = File.open(arg)

   file_data = file.read.to_i

   first = file_data + 3
   second = file_data + 4
   third = file_data + 7
   forth = file_data + 10
   fifth = file_data + 17

   print "#{first} #{second} #{third} #{forth} #{fifth}"

end
```

### Solution Notes:
N.A\
Code walkthrough is still in progress.

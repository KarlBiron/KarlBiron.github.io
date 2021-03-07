---
title: "Ruby Challenge: Its_new_math"
date: 2020-12-05
tags: [Ruby scripting]
header:
  #image: "/images/perceptron/percept.jpg"
excerpt: "Ruby Challenge: Its_new_math"
mathjax: "true"
permalink: /scripting_projects_posts/Ruby_Its_new_math/
---

---
### Task Details:
Execute the code against the input file (somefile.txt).\
The expected output results are below.
```
True:   13 = 14 - 1
True:   2 * 2 = 4
True:   1 * 1 = 1
Error:  10 + b = 22
False:  96 = 24 + 6 / 3 * 5 * 8 - 9
True:   24 + 6 / (3 * 5) * 8 - 9 = 15
True:   0 / 5 = 0
Error:  5 / 0 = 0
True:   99 = 98 + 1
False:  5 = 2 + 2
True:   2 + 2 = 4
True:   -2 + -1.75 = -3.75
False:  -100.0001 = -101 - 1
True:   -100.0001 = -101 - -0.9999
```
---
### Input File Contents (somefile.txt):
```
13 = 14 - 1
2 * 2 = 4
1 * 1 = 1
10 + b = 22
96 = 24 + 6 / 3 * 5 * 8 - 9
24 + 6 / (3 * 5) * 8 - 9 = 15
0 / 5 = 0
5 / 0 = 0
99 = 98 + 1
5 = 2 + 2
2 + 2 = 4
-2 + -1.75 = -3.75
-100.0001 = -101 - 1
-100.0001 = -101 - -0.9999
```

---
### Its_new_math Challenge Solution
```ruby
for arg in ARGV
   file = File.open(arg)

   file_data = file.read
   output = ""

   file_data.each_line do |line|
     eq = line.sub("=","==")
     result = eval eq # true/false result

     if result == true
       output << "True:   #{line}"
     else
       output << "False:  #{line}"
     end
        rescue NameError => ne
          output << "Error:  #{line}"
        rescue ZeroDivisionError => zde
          output << "Error:  #{line}"
   end

   puts output

end
```


### Solution Notes:
N.A\
Code walkthrough is still in progress.

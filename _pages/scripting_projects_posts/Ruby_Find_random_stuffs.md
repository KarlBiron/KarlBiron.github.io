---
title: "Ruby Challenge: Find_random_stuffs"
date: 2020-12-05
tags: [Ruby scripting]
header:
  #image: "/images/perceptron/percept.jpg"
excerpt: "Ruby Challenge: Find_random_stuffs"
mathjax: "true"
permalink: /scripting_projects_posts/Ruby_Find_random_stuffs/
---

---
### Task Details:
Execute the code against the input file (somefile.txt).\
The expected output results are below.
```
14,21,28,42,49,56,63,77,84,91,98
56
```
---
### Input File Contents (somefile.txt):
```
10 100
50 60
```

---
### Find_random_stuffs Challenge Solution
```ruby

final = ""

  for arg in ARGV
     file = File.open(arg)

     file_data = file.read

     file_data.each_line do |line|

       output = ""
       array = []

       array = line.split.map(&:to_i)

       (array.first..array.last).each do |num|
         if (num % 7) == 0 && (num % 5) != 0
           output += "#{num},"
         end
       end
       final += output.delete_suffix(',').concat("\n")
     end
     puts final.strip
  end
```

### Solution Notes:
Convert the string into an array of two integers and then take the first array element to loop through each number until the loop reaches the second/last array element.
The code Checks if the number is divisible by 7 AND not divisible by 5. If so, append the number to the "output" variable
Delete the "," ending for each line and concatenate a new line for each line.
Finally, remove the "\n" from the end of the strings.

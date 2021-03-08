---
title: "Ruby Challenge: Oddly_fibonacci"
date: 2020-12-05
tags: [Ruby scripting]
header:
  #image: "/images/perceptron/percept.jpg"
excerpt: "Ruby Challenge: Oddly_fibonacci"
mathjax: "true"
permalink: /scripting_projects_posts/Ruby_Oddly_fibonacci/
---

---
### Task Details:
Execute the code against the input file (somefile.txt).\
The expected output results are below.
```
7519
```
---
### Input File Contents (somefile.txt):
```
10 20
```

---
### Oddly_fibonacci Challenge Solution
```ruby
def fibonacci(n)
  if n == 1
    1
  elsif n == 2
    1
  else
    fibonacci(n-1) + fibonacci(n-2)
  end
end


for arg in ARGV
   file = File.open(arg)

   file_data = file.read

   array = file_data.split(" ").map(&:to_i)

   range = (array.first..array.last-1).to_a

   total = []

   range.each do |i|
    total << fibonacci(i)
   end

   output = 0

   total.each do |j|
     if j.odd? == true
       output += j
     else
       print ""
     end
   end

puts ""
puts output

end
```


### Solution Notes:
1 (1st value)\
0 + 1 = 1 (2nd)\
1 + 1 = 2 (3rd)\
1 + 2 = 3 (4th)\
2 + 3 = 5 (5th)\
3 + 5 = 8 (6th)\
5 + 8 = 13 (7th)\
8 + 13 = 21 (8th)\
13 + 21 = 34 (9th)\
21 + 34 = 55 (10th)

N.A\
Code walkthrough is still in progress.

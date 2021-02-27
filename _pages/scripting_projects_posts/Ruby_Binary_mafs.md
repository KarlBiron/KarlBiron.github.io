---
title: "Ruby Challenge: Binary_mafs"
date: 2020-12-05
tags: [Ruby scripting]
header:
  #image: "/images/perceptron/percept.jpg"
excerpt: "Ruby Challenge: Binary_mafs"
mathjax: "true"
permalink: /scripting_projects_posts/Ruby_Binary_mafs/
---

---
### Task Details:
Execute the code against the input file (somefile.txt).\
The expected output results are below.
```
15
57
```
---
### Input File Contents (somefile.txt):
```
0b1 0b10 0b11 0b100 0b101
0b1 0b11 0b111 0b1111 0b11111
```

---
### Binary_mafs Challenge Solution
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
Initialize an array (*array[]*) to store the binary values in an ordered manner.\
Use the *each* loop to conduct the operation for each line.\

Array is populated with the binary values.\
The *.strip* method to removes any new line whitespaces.\
The *.split* method is also used to itemize the binary values into the array.\

Modify the array items with the *.each_with_index* method.\
It is used to carry over the item value as well as the index value to conduct the array modification.\

The *Integer()* class used convert the binary values into integer values ready to summation.\

The *.sum* method used to sum all the integers in the array.\

The *array[]* code empties the array for the next iteration on the "each_line" loop.

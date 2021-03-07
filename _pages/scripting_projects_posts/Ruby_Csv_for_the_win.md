---
title: "Ruby Challenge: Csv_for_the_win"
date: 2020-12-05
tags: [Ruby scripting]
header:
  #image: "/images/perceptron/percept.jpg"
excerpt: "Ruby Challenge: Csv_for_the_win"
mathjax: "true"
permalink: /scripting_projects_posts/Ruby_Csv_for_the_win/
---
---
### Task Details:
Execute the code against the input file (somefile.txt).\
The expected output results are below.
```
285.30099
```
---
### Input File Contents (somefile.txt):
```
1,2,3,4,0.1,2.2,12,4.00099,234,5,4,3,2,9
```

---
### Csv_for_the_win Challenge Solution
```ruby
for arg in ARGV
   file = File.open(arg)

   file_data = file.read

   arr = file_data.split(",").map(&:to_f)

   print arr.sum
end
```


### Solution Notes:
Convert a String to An Array of Characters
The *.split(",")* method splits the data into the comma "," delimeter since this text file is in the form of a CSV.
The *.map()* method converts the split file into an array.
The *&:to_f* method converts all the elements within the array to be in the float format.
Finally, the *.sum* method adds all the array elements tp produce the required output.

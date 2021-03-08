---
title: "Ruby Challenge: ORDinary_words"
date: 2020-12-05
tags: [Ruby scripting]
header:
  #image: "/images/perceptron/percept.jpg"
excerpt: "Ruby Challenge: ORDinary_words"
mathjax: "true"
permalink: /scripting_projects_posts/Ruby_ORDinary_words/
---

---
### Task Details:
Execute the code against the input file (somefile.txt).\
The expected output results are below.
```
CWN{Wh0_d03$n't_Lik3_0rDiN@rY_w0rD$}
```
---
### Input File Contents (somefile.txt):
```
67 87 78 123 87 104 48 95 100 48 51 36 110 39 116 95 76 105 107 51 95 48 114 68 105 78 64 114 89 95 119 48 114 68 36 125
```

---
### ORDinary_words Challenge Solution
```ruby
for arg in ARGV
   file = File.open(arg)

   file_data = file.read

   result = file_data.gsub(/\d+/) { |digit| digit.to_i.chr }

   print result.gsub(/ /, "")

end
```


### Solution Notes:
The *to_i* method converts the strings into integers.\
The *.chr* method converts the integers into decimals.

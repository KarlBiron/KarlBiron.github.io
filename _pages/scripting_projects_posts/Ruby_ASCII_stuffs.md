---
title: "Ruby: ASCII Stuffs"
date: 2020-12-05
tags: [Ruby scripting]
header:
  #image: "/images/perceptron/percept.jpg"
excerpt: "Ruby: ASCII Stuffs"
mathjax: "true"
permalink: /scripting_projects_posts/Ruby_ASCII_Stuffs/
---

---
### Task Details:
Execute the code against the input file (somefile.txt).\
The expected output results are below.
```
ABCD?
A B C D!
```
---
### Input File Contents (somefile.txt):
```
41 42 43 44 3f 0a 41 20 42 20 43 20 44 21
```

Download somefile.txt [HERE](C:\Users\Karl\Desktop\GitHub Portfolio\KarlBiron.github.io\_pages\scripting_projects_posts\Ruby_ASCII_stuffs_somefile.txt)
---
### ASCII_stuffs Challenge Solution
```ruby
for arg in ARGV
   file = File.open(arg)

   file_data = file.read

   sanitized = file_data.gsub(" ","")

   result = [sanitized].pack("H*")

   puts result
end
```
---
### NOTES:
The gsub: "g" stands for global and "sub" stands for substitute.\
An alternative solution is the .delete method as shown below.\
⋅⋅⋅a = "\tI have some whitespaces.\t"\
⋅⋅⋅a.delete!(" ")     #=>  "\tIhavesomewhitespaces.\t"\
The H used with the pack method gives you a hex number to string conversion.

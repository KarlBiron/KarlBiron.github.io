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
<br />

---
### NOTES:
The gsub: "g" stands for global and "sub" stands for substitute.\
An alternative solution is the .delete method as shown below.\
    a = "\tI have some whitespaces.\t"\
    a.delete!(" ")     #=>  "\tIhavesomewhitespaces.\t"\

The H used with the pack method gives you a hex number to string conversion.
---

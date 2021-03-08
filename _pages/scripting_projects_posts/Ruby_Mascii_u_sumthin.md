---
title: "Ruby Challenge: Mascii_u_sumthin"
date: 2020-12-05
tags: [Ruby scripting]
header:
  #image: "/images/perceptron/percept.jpg"
excerpt: "Ruby Challenge: Mascii_u_sumthin"
mathjax: "true"
permalink: /scripting_projects_posts/Ruby_Mascii_u_sumthin/
---

---
### Task Details:
Execute the code against the input file (somefile.txt).\
The expected output results are below.
```
This is a line.
This is also a line.
There goes the neighborhood!
```
---
### Input File Contents (somefile.txt):
```
0x54 0x68 105 0b1110011 0b100000 0x69 0x73 0x20 97 32 0x6c 0b1101001 0x6e 0b1100101 0b101110 0b1010 0b1010100 0150 0x69 0b1110011 0b100000 105 0x73 0x20 0b1100001 0b1101100 0b1110011 0157 040 0x61 0x20 0x6c 0b1101001 0x6e 0b1100101 056 012 0x54 104 101 114 0145 040 0b1100111 0157 0145 0b1110011 0b100000 0b1110100 0x68 0145 040 0x6e 0145 105 0147 0x68 0142 0b1101111 114 104 0157 0b1101111 0b1100100 33 10
```

---
### Mascii_u_sumthin Challenge Solution
```ruby
for arg in ARGV
   file = File.open(arg)

   file_data = file.read.split

   file_data.each do |thing|

     converted = ""
     converted = Integer(thing)

     print converted.chr

   end
end
```

### Solution Notes:
The HEX,BIN,OCT,DEC are in the form of String originally, thus it first needs to be formatted into an Integer using the Integer() class\
The *to_i* method does not work for the **converted** variable for integer convertion\
Finally, the *.chr* method only works on an Integer variable.

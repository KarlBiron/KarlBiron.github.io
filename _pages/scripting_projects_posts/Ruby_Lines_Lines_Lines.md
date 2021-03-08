---
title: "Ruby Challenge: Lines_Lines_Lines"
date: 2020-12-05
tags: [Ruby scripting]
header:
  #image: "/images/perceptron/percept.jpg"
excerpt: "Ruby Challenge: Lines_Lines_Lines"
mathjax: "true"
permalink: /scripting_projects_posts/Ruby_Lines_Lines_Lines/
---

---
### Task Details:
Execute the code against the input file (somefile.txt).\
The expected output results are below.
```
this is one line this is also just one line maybe we should try something different ha ha haha
```
---
### Input File Contents (somefile.txt):
```
this is one line

this
is also
just one
line

maybe we should try something different

ha
ha
haha
```

---
### Lines_Lines_Lines Challenge Solution
```ruby
for arg in ARGV
   file = File.open(arg)

   file_data = file.read

   puts file_data.gsub!(/\n/, " ").gsub(/ +/, " ")

end
```

### Solution Notes:
You can use gsub to replace one or more whitespace (regex / +/) to a single whitespace:\
The *.gsub!(/\n/, " ")* method is used to convert all newlines into a single space.

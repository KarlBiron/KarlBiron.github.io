---
title: "Ruby Challenge: Simple_cipher"
date: 2020-12-05
tags: [Ruby scripting]
header:
  #image: "/images/perceptron/percept.jpg"
excerpt: "Ruby Challenge: Simple_cipher"
mathjax: "true"
permalink: /scripting_projects_posts/Ruby_Simple_cipher/
---

---
### Task Details:
Execute the code against the input file (somefile.txt).\
The expected output results are below.
```
We Attack At Dawn
```
---
### Input File Contents (somefile.txt):
```
We are going to the starbucks, time meow. Attack on titan is pretty insane. At 0530, the BN run will start. Dawn is my favorite dish soap, it's totally dope.
```

---
### Simple_cipher Challenge Solution
```ruby
for arg in ARGV
   file = File.open(arg)

   file_data = file.read

   sanitize = file_data.gsub!(".",".\n")

   paragraph = ""

   sanitize.each_line do |line|
     paragraph << line.strip.split.first
     paragraph << " "
   end

   print paragraph

end
```

### Solution Notes:
N.A\
Code walkthrough is still in progress.

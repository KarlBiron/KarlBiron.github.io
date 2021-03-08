---
title: "Ruby Challenge: Forwards_is_backwards"
date: 2020-12-05
tags: [Ruby scripting]
header:
  #image: "/images/perceptron/percept.jpg"
excerpt: "Ruby Challenge: Forwards_is_backwards"
mathjax: "true"
permalink: /scripting_projects_posts/Ruby_Forwards_is_backwards/
---

---
### Task Details:
Execute the code against the input file (somefile.txt).\
The expected output results are below.
```
True
False
False
```
---
### Input File Contents (somefile.txt):
```
radar
creepy
Radar
```

---
### Forwards_is_backwards Challenge Solution
```ruby
for arg in ARGV
  file = File.open(arg)

  file.each_line do |line|
    line.gsub!(/\s/, '')
    if line == line.reverse
      puts "True"
    else
      puts "False"
    end
  end
end
```

### Solution Notes:
Syntax: str.gsub!(pattern, replacement)

---
title: "Ruby Challenge: Simple_addition"
date: 2020-12-05
tags: [Ruby scripting]
header:
  #image: "/images/perceptron/percept.jpg"
excerpt: "Ruby Challenge: Simple_addition"
mathjax: "true"
permalink: /scripting_projects_posts/Ruby_Simple_addition/
---

---
### Task Details:
Execute the code against the input file (somefile.txt).\
The expected output results are below.
```
2
4
6
8
10
-3
10.5
```
---
### Input File Contents (somefile.txt):
```
1 1
2 2
3 3
4 4
5 5
-1 -2
.5 10
```

---
### Simple_addition Challenge Solution
```ruby
for arg in ARGV
  file = File.open(arg)

  file.each_line do |line|

    if line.start_with?('.')
      line.gsub!(" ","+")
      line.gsub!(".","0.")
      puts eval line
    else

    line.gsub!(" ","+")

    puts eval line
    end
  end

end
```

### Solution Notes:
The "if" statement catches any numbers that are in the form of a decimal and converts them into a float format.

---
title: "Ruby Challenge: Scrape_me"
date: 2020-12-05
tags: [Ruby scripting]
header:
  #image: "/images/perceptron/percept.jpg"
excerpt: "Ruby Challenge: Scrape_me"
mathjax: "true"
permalink: /scripting_projects_posts/Ruby_Scrape_me/
---

---
### Task Details:
Execute the code against the input file (somefile.txt).\
The expected output results are below.
```
N.A
```
---
### Input File Contents (somefile.txt):
```
N.A
```

---
### Scrape_me Challenge Solution
```ruby
require 'open-uri'

for arg in ARGV

   URI.open(arg) {|f|
     f.each_line {|line| puts line.chomp}
   }

end
```


### Solution Notes:
N.A\
Code walkthrough is still in progress.

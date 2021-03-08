---
title: "Ruby Challenge: White_socks_with_boots"
date: 2020-12-05
tags: [Ruby scripting]
header:
  #image: "/images/perceptron/percept.jpg"
excerpt: "Ruby Challenge: White_socks_with_boots"
mathjax: "true"
permalink: /scripting_projects_posts/Ruby_White_socks_with_boots/
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
### White_socks_with_boots Challenge Solution
```ruby
require 'socket'

for i in 0 ... ARGV.length

   hostname = "#{ARGV[0]}"
   port = "#{ARGV[1]}".to_i

   s = TCPSocket.open(hostname, port)

   while line = s.gets
     print line.chomp
   end
  s.close

break

end
```


### Solution Notes:
puts "#{i} #{ARGV[i]}"\
=>  0 listen.runcode.ninja\
=>  1 9005

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

# H1 Heading
# Ruby Challenge: White_socks_with_boots

Ruby Code Solution:
```ruby
require 'socket'

for i in 0 ... ARGV.length
   #puts "#{i} #{ARGV[i]}"
   #=>  0 listen.runcode.ninja
   #=>  1 9005

   hostname = "#{ARGV[0]}"
   port = "#{ARGV[1]}".to_i

   #puts hostname
   #puts port

   s = TCPSocket.open(hostname, port)

   while line = s.gets
     print line.chomp
   end
  s.close

break

end
```

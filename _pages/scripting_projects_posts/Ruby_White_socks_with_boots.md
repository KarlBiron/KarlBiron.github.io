---
title: "Ruby Basics"
date: 2020-12-05
tags: [Ruby scripting]
header:
  #image: "/images/perceptron/percept.jpg"
excerpt: "Ruby Basics"
mathjax: "true"
permalink: /scripting_projects_posts/Ruby_Basics/
---

# H1 Heading
# Ruby Basics

## H2 Heading

### H3 Heading

"Hello World" Ruby:
```ruby
puts "Hello, World!"
```

"Argumentative" Ruby:
```ruby
for i in 0 ... ARGV.length
   print "#{ARGV[i]} "
end
```

"Here_Kitty" Ruby:
```ruby
for arg in ARGV
   file = File.open(arg)

   file_data = file.read

   puts file_data
end
```

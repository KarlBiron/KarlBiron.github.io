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


---
>  <font size="2"> <b>Note</b>: Do not forget to include the Ruby Shebang "<b>#!/usr/bin/env ruby</b>" on top of each of the Ruby files for it to run successfully.
I do not have the Shebang in the code sections as this will be repetitive and it also cause a display error in the Markdown code of this blog. </font>

---
### "Hello World" Ruby:
The initial "Hello World" code to test if all environment and setup is done successfully.
```ruby
puts "Hello, World!"
```

---
### "Argumentative" Ruby:
A code that tests user inputs though CLI. In this case, the user can input multiple values delimited by a space.
```ruby
for i in 0 ... ARGV.length
   print "#{ARGV[i]} "
end
```

---
### "Here_Kitty" Ruby:
A code that tests user FILE inputs though CLI. In this case, the user can input multiple FILES delimited by a space.
```ruby
for arg in ARGV
   file = File.open(arg)

   file_data = file.read

   puts file_data
end
```

---

---
title: "Ruby: ASCII Stuffs"
date: 2020-12-05
tags: [Ruby scripting]
header:
  #image: "/images/perceptron/percept.jpg"
excerpt: "Ruby: ASCII Stuffs"
mathjax: "true"
permalink: /scripting_projects_posts/Ruby_ASCII_Stuffs/
---

# H1 Heading
# Solving "ASCII Stuffs" in RunCode.Ninja with Ruby

## H2 Heading

### H3 Heading

What about a [link](https://github.com/KarlBiron)

Ruby code block:
```ruby
#!/usr/bin/env ruby

for arg in ARGV
   file = File.open(arg)

   file_data = file.read

   # gsub: "g" stands for global
   # and "sub" stands for substite
   # Alternative solution is the .delete
   # Ruby method as shown below:
   # a = "\tI have some whitespaces.\t"
   # a.delete!(" ")     #=>  "\tIhavesomewhitespaces.\t"
   sanitized = file_data.gsub(" ","")

   # The H used with the pack method gives
   # you a hex number to string conversion.
   result = [sanitized].pack("H*")

   puts result
end
```

```ruby
require 'redcarpet'
markdown = Redcarpet.new("Hello World!")
puts markdown.to_html
```
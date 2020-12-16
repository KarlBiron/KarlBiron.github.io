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

# H1 Heading
# Ruby Challenge: Scrape_me

Ruby Code Solution:
```ruby
require 'open-uri'

for arg in ARGV

   URI.open(arg) {|f|
     f.each_line {|line| puts line.chomp}
   }

end
```

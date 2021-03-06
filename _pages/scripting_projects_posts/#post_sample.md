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

Here's some basic text.

And here some *italics*.

Here's some **bold** text.

What about a [link](https://github.com/KarlBiron)

Here's a bulleted list:
* First item
+ Second item
- Third item

Here's a numbered list
1. First
2. Second
3. Third

Ruby code block:
```ruby
for arg in ARGV
   file = File.open(arg)

   file_data = file.read

   sanitized = file_data.gsub(" ","")

   result = [sanitized].pack("H*")

   puts result
end
```

Python code block:
```python
    import numpy as np

    def test_function(x, y):
      z = np.sum(x,y)
      return z  
```

R code block:
```r
library(tidyverse)
df <- read_csv("some_file.csv")
head(df)
```

Here's some inline code `x+y`.

Here's some math:

$$z=x+y$$

You can also put it inline $$z=x+y$$

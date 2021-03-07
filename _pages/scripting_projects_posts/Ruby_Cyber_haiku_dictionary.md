---
title: "Ruby Challenge: Cyber_haiku_dictionary"
date: 2020-12-05
tags: [Ruby scripting]
header:
  #image: "/images/perceptron/percept.jpg"
excerpt: "Ruby Challenge: Cyber_haiku_dictionary"
mathjax: "true"
permalink: /scripting_projects_posts/Ruby_Cyber_haiku_dictionary/
---

---
### Task Details:
Execute the code against the input file (somefile.txt).\
The expected output results are below.
```
We're good - we used strong encryption.
You're just talking about theoretical concerns.
Yes, TLS is enabled by default
My Wordpress instance is completely secure
InfoSec Masters degree: "What's a botnet?"
```
---
### Input File Contents (somefile.txt):
```
{'24': 'Wordpress', '25': 'instance', '26': 'is', '27': 'completely', '20': 'by', '21': 'default', '22': '\n', '23': 'My', '28': 'secure', '29': '\n', '1': "We're", '3': '-', '2': 'good', '5': 'used', '4': 'we', '7': 'encryption.', '6': 'strong', '9': "You're", '8': '\n', '11': 'talking', '10': 'just', '13': 'theoretical', '12': 'about', '15': '\n', '14': 'concerns.', '17': 'TLS', '16': 'Yes,', '19': 'enabled', '18': 'is', '31': 'Masters', '30': 'InfoSec', '36': '\n', '35': 'botnet?"', '34': 'a', '33': '"What\'s', '32': 'degree:'}
```

---
### Cyber_haiku_dictionary Challenge Solution
```ruby
for arg in ARGV
   file = File.open(arg)

   file_data = file.read

   hash = eval(file_data)

   fixed = hash.sort_by { |num, word| num[/\d+/].to_i }

   sanitize = fixed.map {|row| row[1]}

   puts sanitize.join(' ').gsub(" \\n ","\n").sub(" \\n","")
end
```


### Solution Notes:
After the *.sort_by* method, the hash has now become an array for some reason.
Since the hash has been turned into an array, we used the "map" method to extract the 2nd column values using row[1] to produce a single row array that has the each row value as an element in the new array./
The single row array is then separated by the *.join(' ')* method which as delimeted by a space and sanitized further with the *.gsub* and *.sub* methods.

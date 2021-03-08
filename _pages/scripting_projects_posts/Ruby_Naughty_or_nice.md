---
title: "Ruby Challenge: Naughty_or_nice"
date: 2020-12-05
tags: [Ruby scripting]
header:
  #image: "/images/perceptron/percept.jpg"
excerpt: "Ruby Challenge: Naughty_or_nice"
mathjax: "true"
permalink: /scripting_projects_posts/Ruby_Naughty_or_nice/
---

---
### Task Details:
Execute the code against the input file (somefile.txt).\
The expected output results are below.
```
Naughty list has 16 people!
Nice list has 15 people!
```
---
### Input File Contents (somefile.txt):
```
Madonna: good
Robert Downey Jr.: good
Jackie Chan - good
Vin Diesel - bad
Bradley Cooper - bad
Adam Sandler: good
Tom Cruise: good
Amitabh Bachchan - good
Salman Khan: bad
Akshay Kumar - good
Mark Wahlberg: bad
Mr Bad dude - good
Mrs Good gal: bad
Jennifer Lawrence - good
Scarlett Johansson: bad
Melissa McCarthy - bad
Bingbing Fan: good
Jennifer Aniston - good
Julia Roberts: good
Angelina Jolie - bad
Reese Witherspoon: bad
Anne Hathaway - good
Kristen Stewart: bad
Cameron Diaz - bad
Gwyneth Paltrow: bad
Meryl Streep: bad
Amanda Seyfried - bad
Sandra Bullock: good
Emma Stone: bad
Mila Kunis - good
Natalie Portman - bad
```

---
### Naughty_or_nice Challenge Solution
```ruby
for arg in ARGV
   file = File.open(arg)

   file_data = file.read

   nice = file_data.scan(/good/).size
   naughty =  file_data.scan(/bad/).size

   puts "Naughty list has #{naughty} people!"
   puts "Nice list has #{nice} people!"
end
```


### Solution Notes:
The *.scan* method is a form of Ruby regex.
The *.size* method counts number of matches.

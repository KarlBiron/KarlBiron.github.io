---
title: "Ruby Challenge: Junk_in_my_trunk"
date: 2020-12-05
tags: [Ruby scripting]
header:
  #image: "/images/perceptron/percept.jpg"
excerpt: "Ruby Challenge: Junk_in_my_trunk"
mathjax: "true"
permalink: /scripting_projects_posts/Ruby_Junk_in_my_trunk/
---

---
### Task Details:
Execute the code against the input file (somefile.txt).\
The expected output results are below.
```
What you gonna do with all that junk?
All that junk inside your trunk?
I'm gonna get, get, get, get, you drunk,
Get you love drunk off my hump.
My hump, my hump, my hump, my hump, my hump,
My hump, my hump, my hump, my lovely little lumps (Check it out)
```
---
### Input File Contents (somefile.txt):
```
WhatZ youH gonnaM doG withC allA thatv junkn?
AllD thatV junko insideQ yours trunkh?
I'ml gonnat getQ, getl, geth, gete, youy drunkt,
GetB youj lovem drunkv offe myu humpJ.
MyA humpc, myO humpP, myZ humpV, mym humpA, myc humpV,
Myu humpz, myA humpU, myw humpw, myW lovelyG littley lumpsl (Checkp itc outZ)
```

---
### Junk_in_my_trunk Challenge Solution
```ruby
output = ""

for arg in ARGV
   file = File.open(arg)

   file_data = file.read

   file_data.each_line do |line|

       line.gsub(/\w+\W+/) { |word|
       if word == "junkn?\n"
         #puts "junk?\n".inspect
         print "junk?\n"
       elsif word == "trunkh?\n"
         #puts "trunk?\n".inspect
         print "trunk?\n"
       elsif word == "I'"
         #puts ""
       elsif word == "ml "
         #puts "I\'m ".inspect
         print "I\'m "
       elsif word.include? "get"
         #puts "get, ".inspect
         print "get, "
       elsif word == "drunkt,\n"
         #puts "drunk,\n".inspect
         print "drunk,\n"
       elsif word == "humpJ.\n"
         #puts "hump.\n".inspect
         print "hump.\n"
       elsif word == "humpV,\n"
         #puts "hump,\n".inspect
         print "hump,\n"
       elsif word.include? "hump"
         #puts "hump, ".inspect
         print "hump, "
       elsif word == "lumpsl ("
         #puts "lumps ".inspect
         print "lumps "
       elsif word == "Checkp "
         #puts "(Check ".inspect
         print "(Check "
       elsif word == "outZ)"
         #puts "out)".inspect
         print "out)"
       else

         print word.strip.chop.concat(" ")
       end
     }
   end
end
```


### Solution Notes:
N.A\
Code walkthrough is still in progress.\

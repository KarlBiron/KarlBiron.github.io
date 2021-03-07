---
title: "Ruby Challenge: Just_a_ord_friend"
date: 2020-12-05
tags: [Ruby scripting]
header:
  #image: "/images/perceptron/percept.jpg"
excerpt: "Ruby Challenge: Just_a_ord_friend"
mathjax: "true"
permalink: /scripting_projects_posts/Ruby_Just_a_ord_friend/
---

---
### Task Details:
Execute the code against the input file (somefile.txt).\
The expected output results are below.
```
71017
```
---
### Input File Contents (somefile.txt):
```
So I took blah - blah's word for it at this time
 I thought just havin' a friend couldn't be no crime
  'Cause I have  friends and that's a fact
 Like Agnes, Agatha, Germaine, and Jacq
Forget about    that, let's go into the story
 About a girl named blah-blah-blah that adored me
  So we         started talkin', getttin' familiar
   Spendin' a lot of time so we can build up
    A relationship or some understanding
   How it's gonna be in the future we was plannin'
  Everything sounded so dandy and sweet
 I had no idea  I was in for a treat
After this was established, everything was cool
 The tour was over and she went back to school
  I called every day to see how she was doin'
   Every time that I called her it seemed somethin' was brewin'
    I called her on my dime, picked up, and then I called again
   I said, yo, who was that? Oh, he's just a friend
  Don't gimme that, don't ever gimme that
Jus' bust       this
```

---
### Just_a_ord_friend Challenge Solution
```ruby
for arg in ARGV
   file = File.open(arg)

   file_data = file.read.gsub!(/\n/, " ").inspect

   total = 0

   file_data.each_char do |char|

     if (/^[a-z]*$/ === char) == true || (/^[A-Z]*$/ === char) == true

       new = char.ord.to_i

       total += new

     else
     end

   end

   puts total

end
```

### Solution Notes:
Based on the ASCII table the "new line" character has an ORD value which causes problems with this task  as shown below:\
"10  LF  (NL line feed, new line)""\
Therefore, its must be removed using the method *.gsub!(/\n/, " ")*\

The **total** variable will be used to sum up all the valid ORD integers within the each loop.\

Use the "each_char" to go through each character individually.\

The "if-else" statement will be used to test out valid characters. \
The *===* operation produce a true/false result.\

The *.ord* method is used to convert the character into a decimal value.\

 The *total += new* adds the new value to the total values accumulated with each iteration.\

---
title: "Ruby Challenge: Dream_slice"
date: 2020-12-05
tags: [Ruby scripting]
header:
  #image: "/images/perceptron/percept.jpg"
excerpt: "Ruby Challenge: Dream_slice"
mathjax: "true"
permalink: /scripting_projects_posts/Ruby_Dream_slice/
---

---
### Task Details:
Execute the code against the input file (somefile.txt).\
The expected output results are below.
```
Over and over again
I relive the moment
I am bearing the burden within
Open wounds hidden under my skin

Pain is real as a cut that bleeds
The face I see every time I try to sleep
Staring at me crying
```
---
### Input File Contents (somefile.txt):
```
inaag vOre nad vore
omemtn I erilev hte
iwhtni I ma ngbeiar hte ubdrne
ksni pOne ownusd ihddne erdun ym

lbeesd aPni si erla sa a uct htta
epesl hTe afec I ese ryeev item I rty ot
rciygn ngStiar ta em
```

---
### Dream_slice Challenge Solution
```ruby
output = ""

for arg in ARGV
   file = File.open(arg)

   file_data = file.read

   file_data.each_line do |line|

     line_order = line.split(" ").map(&:to_s).rotate(1)

     line_order.each do |word|

       char_order = []

       if word.size == 1

         output += word.concat(" ")
       elsif word.size == 2
         order = [1,0]

         output += order.map{|x| word[x]}.join().concat(" ")
       elsif word.size == 3
         order = [1,0,2]

         output += order.map{|x| word[x]}.join().concat(" ")
       elsif word.size == 4
         order = [1,0,3,2]

         output += order.map{|x| word[x]}.join().concat(" ")
       elsif word.size == 5
         order = [3,4,2,0,1]

         output += order.map{|x| word[x]}.join().concat(" ")
       elsif word.size == 6
         order = [1,0,3,2,5,4]

         output += order.map{|x| word[x]}.join().concat(" ")
       elsif word.size == 7
         order = [2,3,5,6,4,0,1]

         output += order.map{|x| word[x]}.join().concat(" ")
       else

       end

     end

     output += "\n"
   end

   puts output.gsub!(" \n\n","\n \n").gsub!(" \n","\n").strip
end
```

### Solution Notes:
Resets the character order variable for ever loop iteration of each word.

---
title: "Ruby Challenge: Confucius_grammar"
date: 2020-12-05
tags: [Ruby scripting]
header:
  #image: "/images/perceptron/percept.jpg"
excerpt: "Ruby Challenge: Confucius_grammar"
mathjax: "true"
permalink: /scripting_projects_posts/Ruby_Confucius_grammar/
---

---
### Task Details:
Execute the code against the input file (somefile.txt).\
The expected output results are below.
```
It does not matter how slowly you go so long as you do not stop.
Our greatest glory is not in never falling, but in rising every time we fall.
I hear and I forget. I see and I remember. I do and I understand.
Wheresoever you go, go with all your heart.
By three methods we may learn wisdom: first, by reflection, which is noblest; second, by imitation, which is easiest; and third by experience, which is the bitterest.
I want you to be everything that's you, deep at the center of your being.
When anger rises, think of the consequences.
He who learns but does not think, is lost. He who thinks but does not learn is in great danger.
Real knowledge is to know the extent of one's ignorance.
When it is obvious that the goals cannot be reached, don't adjust the goals, adjust the action steps.
Before you embark on a journey of revenge, dig two graves.
```
---
### Input File Contents (somefile.txt):
```
It dOEs nOt mAttEr hOw slOwly yOU GO SO lOng As yOU dO nOt stOp.
OUr grEAtEst glOry is nOt In nEvEr fAllIng, bUt In rIsIng EvEry tImE wE fAll.
I hEAr And i fOrgEt. I sEE And I rEmEmbEr. I dO And I UndErstAnd.
WhErEsOEvEr yOU gO, gO wIth All yOUr hEArt.
By thrEE mEthOds wE mAy lEArn wIsdOm: fIrst, by REflEctIOn, whIch Is nOblEst; sEcOnd, by ImItAtIOn, whIch is EAsIEst; And thIrd by ExpErIEncE, whIch Is ThE bIttErEst.
I wAnt yOU tO bE EvErythIng thAt's yOU, dEEp At thE cEntEr of yOUr beIng.
WhEn angEr RIsEs, ThInk Of thE cOnsEqUEncEs.
hE whO lEArns bUt dOEs nOt thInk, Is lOst. HE whO thInks bUt dOEs nOt lEArn Is In grEAt dAngEr.
REAl knOwlEdgE Is tO knOw thE ExtEnt Of OnE's IgnOrAncE.
WhEn iT Is ObvIOUs that the GoaLS CAnnOt bE rEAchEd, dOn't AdjUst thE gOAls, AdjUst thE ActIOn stEps.
BEFOrE YOU EmbArk On A jOUrnEy Of rEvEngE, DIg twO grAvEs.
```

---
### Confucius_grammar Challenge Solution
```ruby
for arg in ARGV
   file = File.open(arg)

   file_data = file.read

   file_data.each_line do |line|
     puts line.downcase.sub(/^./, &:upcase).gsub(" i "," I ").sub(" he "," He ")
   end
end
```

### Solution Notes:
The *.downcase* method converts all alphabetical strings into lower case characters.
The *.sub(/^./, &:upcase)* method takes beginning characters of each line and then converts them into uppercase characters.
The *.gsub(" i "," I ")* method globally convert all "i" into "I" characters for grammatical correctness.
The *.sub(" he "," He ")* method converts all "he" into "He" for grammatical correctness.

# v0.2.0 Unstable - The Protocol Update
#### This Update - I completely remake the core AND indroduce not 1 but 18 awesome protocols
---
##### lines of code: 334
##### made in (time): 5hrs 47min
---
This update is an "unstable" update. It's basically a demo which visually shows you 
how the new protocols work.
###The Protocols:
First of all, as soon as you launch the program, it will search for a file called "sample.txt" 
in the same directory as the program. If it fails to find a file with that exact name - you shall see a an Unhandled Exception Error message. I'll let you be able to specify the file later

Having done that, it will now read the file and create two txt files in the same directory of the program called 
"CICHICHICHCIHIPAHIH" and "LOGGOGOGOO". If you open the file, you'll see that "CICHICHICHCIHIPAHIH" has all the questions and "LOGGOGOGOO" has all the answers. (This took me about 2 hours to make, by the way)

Although this program is closed source - I feel generous so I'll give the first line and last line of code away:
```C#
  #region TMP qqs
  #endregion
```
It works by copying the txt file to your memory - but missing out alternate lines. It then creates the file "CICHICHICHCIHIPAHIH" by writing the memory onto the hard drive. It does this again but with an offset of 1 line. Thus you now have two files, one with answers and one with questions.

Moving swiftly on, now the code has to do a couple of things. First of all, it must remove 'special' characters from the question. In my code, this is referenced as filtering. The filter removes characters such as "(" ")" "+" "/" etc
The questions' formatting is different to the answer formatting so they must both go through their own specialised filters 
(one of the main reasons why I decided that the code should generate seperate "answers" and "questions" files).

Let's say for example a question in the file reads "consilium, consilii (n)"
The filter will remove the special characters so it then becomes - "consilium consilii n"

The answers filter is different, like I said. The answers' are formatted that each answer is seperated by a slash if they have more than one answer. The answers' filter is very similar to that of the questions yet not same.

Now, the code has to split up the question/answer into an array. 

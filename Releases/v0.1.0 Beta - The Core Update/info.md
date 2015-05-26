# v0.1 Beta - The Core Update
### This is the first ever version of VTPX!
---
##### lines of code: 247
##### made in (time): 2hrs 30min
---

Currently, when you launch it - there is no user interface.
It appears to be just a terminal with the lines of text
"Hello World!"
and
"Translate: love/like"

Of course, the finished VTPX will look absolutely nothing like this.
By the way - it only says "Hello World!" because that was a test.
I've decided to keep it there :)

This first version is only showcasing the very basic marking system.
The marking system currently:
* Ignores excess characters
* Detects whether or not you missed out words
* Tells you which words you got wrong
* If you don't give the specified amount of arguments - it doesn't go bezerk and force close (unlike before in Alpha testing)
* Does not care about capitalisation of letters

Test the features!
For now, it only has 1 question - which is "Translate: love/like"
(the answer is amo, amare, amavi, amatum by the way)

## Here's the output if you enter the following things:
### Amo, Amare, Amavi, Amatum
```
Hello World! 
translate: love/like 
amo, amare, amavi, amatum 
4 arguments are required 
You gave 4 arguments 
Here are the words you typed: 
amo, amare, amavi, amatum 
Now marking your work: 
amo, True 
amare, True 
amavi, True 
amatum True 
Did you get the words you answered all right? 
True 
Did you get the whole question right? 
True 
```
### Amo, Amare, Amavi
```
Hello World! 
translate: love/like 
AMo, AmArE, aMaVI 
4 arguments are required 
You gave 3 arguments 
Now marking your work: 
You only said 3 words, here's what you got: 
AMo, True 
AmArE, True 
aMaVIi True 
Did you get the words you answered all right? 
True 
Did you get the whole question right? 
False 
Reason: You did not do all the words required 
```
(as you can see, capitalisation does not matter)

### Emo, Amare, Amui, Amatum
```
Hello World! 
translate: love/like 
Emo, Amare, Amui, Amatum 
4 arguments are required 
You gave 4 arguments 
Here are the arguments you gave:
Emo,
Amare,
Amui,
Amatum
Now marking your work:  
Emo, False 
Amare, True 
Amui, False
Amatum True 
Did you get the words you answered all right? 
False 
Did you get the whole question right? 
False 
Reason:
You got the following answers wrong:
amo
amavi
```
### Emo, Amare, Amui
```
Hello World! 
translate: love/like 
Emo, Amare, Amui 
4 arguments are required 
You gave 3 arguments 
Now marking your work: 
You only said 3 words, here's what you got: 
Emo, False 
Amare, True 
Amui False
Did you get the words you answered all right? 
False 
Did you get the whole question right? 
False 
Reason:
You did not do all the answers required
also, you got the following answers wrong:
amo
```

##Also...
Bear in mind that the marking system works by using
the Contains(); method in C# - This means that if you write

GuhSU543IgeGHI2£()BDdb&%$$DJkug**AmO**ihah234UHIU&&£Sghusihi56u2890{]"£&()"4645[~@.5><>82^%"$$£"]}

as your answer - it shall be marked right. Look closely, "amo" is in there somewhere ;)

this does have its negatives, though. Because if you thought "amo" was "amoe" - amoe shall be marked right

## How to exit?
By the way, if it wasn't obvious enough - you press the "X" button to exit.
Or you can press enter once the question has been answered.

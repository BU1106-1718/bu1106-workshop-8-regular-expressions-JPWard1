# BU1106 Task Regular Expressions

## Introduction

### Overview

This week you get to work on some regex examples. 

### Editing

You can create documents and edit them directly in GitHub's web interface. This is a very convenient way of creating and editing the files. 
In most cases, the preferred way of working is to create and edit the files on your own machine. 

In the next weeks we will have to work with files in a programme (R and R Studio) that we will install on our machines, so GitHub Desktop will become the preferred way of working on our repositories. To get used to GitHub Desktop please make at least one of your commits through GitHub Desktop. You can do all your commits in GitHub Desktop if you want.    

## Task Explanation

Below is today's task. We will be working with regular expressions. 
If you want a reminder how regular expressions work you can [watch parts of last week's class again on YouTube](https://www.youtube.com/watch?v=Qwy4WOqkRYk).

For this task, you need to provide the answers in the file you are currently reading. It is a Markdown file. More explanations about the Markdown syntax can be found [on GitHub's Mastering Markdown page](https://guides.github.com/features/mastering-markdown/).

* Under the heading _Your Task_ you will find several questions. 
* Try to find the regular expressions needed to fulfil the criteria. 
  * You might want to use Notepad++ or a website like [regular expressions 101](https://regex101.com/) or [RegExr](https://regexr.com/) to test your regular expressions. 


**Commit early, commit often** - that way you can go back if you have made a mistake and I can see all the work you have done. It doesn't matter if your early commits contain mistakes.  

Once you are done be sure to commit your changes (that will save them to the repository) and to push them to GitHub (so that I can see the work you have done).


## Your Task

#### Question 1

A UCLan student number looks like this: G31415926. 

Find a regular expression that will match a student number.
 
`Hint: The numbers are (obviously) different for different students, so finding a regular expression that only matches this one student number is not enough. 
Unless the way your regular expression works is obvious, please explain how it works.`

**Answer:** G\d\d\d\d\d\d\d\d   -  Start with capital "G" followed by 8 digits 0-9 "\d" x 8 times
Ammended to correctionj - \bG\d\d\d\d\d\d\d\d\b - needs "\b" at start and end to signify word boundary

#### Question 2

Sometimes people will write the G as a lower case character or leave out the letter altogether. 
Find a regular expression that will match a student number, based on the additional information presented in this question. 
 
`Hint: Unless the way your regular expression works is obvious, please explain how it works, e.g. this here will match the character and that here makes sure it also works if there is no character in front of the number.`

**Answer:** \bG?g?\d\d\d\d\d\d\d\d\b - Adding ? to deliver true or false for g OR G

#### Question 3

Sometimes you see other letters in front of the number (instead of G), e.g. if students sign up for a certificate that will not form part of their degree classification. 
Find a regular expression that will match a student number, based on the additional information presented in this question. 
 
`Hint: Unless the way your regular expression works is obvious, please explain how it works.`

**Answer:** \b\w?\d\d\d\d\d\d\d\d\b  - now states you can/or not have a letter followed by 8 digits.

#### Question 4a

Think of different ways of writing down a British phone number. and write them down as your answer to this question (one per line).

Example: (01772) 201201, +44 (0)1772 201201  
 
`Hint: It's obvious, but just to spell it out: For this question, you should think about different ways of writing down a phone number. It's not about trying to come up with as many phone number as you can.`

**Answer:** 
01772 234567
01772234567
(01772) 234567
(01772)234567
01772-234567
+44 1772 234567
+44 1772234567
+44 (0)1772 234567
+44 (0)1772234567
+44 1772-234567
+44 (0)1772-234567
+4417722 234567
+441772234567
+44(0)1772 234567
+44(0)1772234567
+44(0)1772-234567

#### Question 4b

Find a regular expression that matches all of the different phone number formats from Question 4a. If you cannot match all try to match as many as possible. If you can't match all, don't change Question 4a by pretending you came up with fewer phone number formats, but you matched them all. It's better if you come up with lots of formats you can't match than if you only come up with very few formats, but you can match all. 
 
`Hint: Unless the way your regular expression works is obvious, please explain how it works.`

**Answer:** '(\+44)?0?(\(0\))?\s?\(?\d{1,5}\)?\s?\-?(\d{6})?\n'

This states

'+44 - yes or no  - followed by'
'0 - y/n'
'(0) - y/n'
'"space" - y/n'
'"(" - y/n'
'1 - 5 digits - y/n'
'"space" - y/n'
'"-" - y/n'
'6 digits - y/n'

This works for the example list I made but will defo not be comprehensicve or fool proof.

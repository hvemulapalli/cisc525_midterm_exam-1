# A Midterm Exam CISC 525 Big Data Architecture - Spring 2020
This is your midterm exam. The exam is worth 20% of your final grade.
Please make effort to complete it as much as you can.

This is a Python project. It contains a single program that makes indexes from text files.

## Run command
To run the application, you must make sure that Hadoop is running with 
the Shakespeare's tragedy plays are properly stored in the `/user/student/shakespeare/tragedy` 
folder (`hint`: use `cisc-525-util`). The comnmand to run is as follows:

```shell script
cd cisc_525
git clone https://github.com/drkiettran/cisc525_midterm_exam
cd cisc525_midterm_exam
./index_maker.py /user/student/shakespeare/tragedy /tmp/tragedy
```
The output are index files that contains one word per line and the line numbers of the original text file that
contains the words. For example, if I was to examine the index file for the play Othello (**othello.txt**), 
I would find this line:
```
accidents [859, 6399]
```
This means that I would find two occurrences of the word `accidents` in the play and they are located on lines
`858` and `6399`.

## Part I (70%)
The activities for this part are as follows:

1. Review the program closely and make sure you understand the program fully.
2. Use `MS WORD` to write a report that explains how the application works. Be sure to include the following
items

    - On each section of the code (functions/methods & significant portion of code inside them), 
    explain in `great` details as to how it works. Assume the reader has little experience in HDFS and
    searching methods. The reader is an experienced Python programmer. In other words, I am not 
    interested in how Python works but in how the application work.
    - Include diagrams (UML, PowerPoint, draw.io, etc.) and screenshots to support your writings. For example
    show me how this program interact with the HDFS file system and/or the node manager, resource manager, etc.
    - Provide `critical` (not `nasty` or `unprofessional`) evaluation of the code and propose a better
    solution. Please `do not just say the code is good and I have no comment`! That will not get you
    a very good grade. Provide me with three (3) possible improvements. 

3. Implement the improvements you provided in section 2 above. Commit and push your `private` repository to
github. **Make sure to share your repository with me!**

## Part II (30%)
The activities for this part are as follows:

1. **Write a Searcher (15%)**

Write a search program and name it `searcher.py` that runs after the `index_maker.py` program (hint: copy 
the index_maker.py to searcher.py). This program should take input from the keyboard. I recommend to make it 
work with only a `single word`. For example search for the word `beseech`. The program should exits, when the
input word is `***exit***`. The program should take the same command line arguments as that of the `index_maker.py`.
The output of a search is simply the name of the original file(s) that contains the word and the lines where the
word was found. Example output is as follows:

```shell script
./searcher.py /user/student/shakespeare/tragedy /tmp/tragedy
>>>  input: accidents
>>> output: othello.txt
 859: Of moving accidents by flood and field
6399: These bloody accidents must excuse my manners,

>>> output: cleopatra.txt
6200:     But accidents unpurposed. Draw, and come.
6789:     Which shackles accidents and bolts up change;

>>> output: hamlet.txt
...etc
```

Note that the word `accident` occurs in more than one plays as shown here:

```text
cleopatra.idx:accidents [6200, 6789]
hamlet.idx:accidents [6172]
othello.idx:accidents [859, 6399]
romeo-and-julitet.idx:accidents [5462]
```

2. **Search for more than one words (15%)**

Update the searcher.py program in section #1 to take in one or more words. Similar to section #1, 
print out the lines of the original text that have one of the search words.

3. You must write a report for this section in addition to your work in sections above.
     

## Submission

- You must make sure your report to include all parts (Part I and Part II).
- You must make sure to provide the **url** of your repository in your report. All work should be in **ONE** repository
- You must make sure that I **accepted** your github invite!

- **DUE DATE is MIDNIGHT Sunday 21 June 2020**
- **NO EXTENSION IS ALLOWED**
- **Individual work only!**

 
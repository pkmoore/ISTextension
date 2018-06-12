# Evaluation
Our goal with this work was to gain an undestanding of how CrashSimulator's user
exprience compared to other tools and techniques available to developers...

Because CrashSimulator is able to to test a wide domain of operations an
appliation can peform we felt it necessary to compare it with two separte tools,
one that test based on files and one that tests based on network activity.
Specifically, we used AFL and Mutiny...

### AFL
AFL is a file-based fuzzer.  It is able to take an input file, mutate its
contents, and pass the file along to the application under test.  AFL is able to
manipulate the contents of files only while CrashSimulator is able to
maniupluate other aspects present in the results and side effects of system
calls.

### Mutiny Fuzzer
Mutiny fuzzer is a network fuzzer operates by mutating and replaying pcap
recordings of network activity.  The similarities between the operation of
Mutiny and CrashSimulator mean that it is a good candidate for comparison.  The
major difference between these two that CrashSimulator can manipulate aspects of
system calls than the messages sent across a network.  Mutiny, on the other
hand, is limited to manipulating the content of messages only.

## Method
The 20 participants in this study received instruction on the configuration and
usage of the above tools as well as CrashSimulator.  We asked these users to
test popular real-world applications with the goal of identifying new bugs and
reporting them to the application's developers.  In performing this task our
participants had to correctly set up and configure each of the tools, execute a
testing process, evaluate the results, and produce sufficient proof of validity
for each bug that a convincing case for fixing it can be made.  Each of these
steps is an opportunity for gaining insight into how CrashSimulator stacks up
against other tools.

We used 3 techniques to capture the experience of our participants as they used
each of the tools.  For quantitative concerns we examined the time required for
participants to carry out defined tasks relevant to the process of bug hunting.
To do this, we asked users to track the time required to perform each step of
the process of finding and reporting a bug. 


We also captured hard counts of bugs identified by our particpants using each of
the tools.  The specifics of these bugs will be discussed in more detail......

For Qualititative concerns we gathered participant impressions on the tools in
use via surveys.  These surveys were strucured to give insight into how
CrashSimlator compares to the other tools in three areas:
* Usability of the tool. (i.e. set up, configuration, executing tests,
  interpretring results)
* Extending the tool
* How well the tool is able to test the areas of an application that they are
  interested in

Additionally, we asked our partipants to rate their own experience level in
software development, software testing, and operating systems concepts so that
we might determine whether or not a participant's background has an effect on
what tools they prefer.

In this evaluation we set out to answer the following questions using both the
qualitiative and quantitative data collected during our study.

1. Are users able to effectively find bugs using CrashSimulator?  How does
CrashSimulator compare to other tools in this area?

2. How well does CrashSimulator allow users to test the areas of applications
   they are interested in?  Are other tools able to better evaluate these areas?

3. Does CrashSimulator allow its users to construct a test suite efficiently?  How
does CrashSimulator compare to similar tools efficiency wise?

4. Does user experience level have an impact on tool experience?  Is there a
difference in the skillsets required in order to be effective with
CrashSimulator vs the other tools?


---

## Are users able to effectively find bugs using CrashSimulator?

For any testing tool or technique the primary concern is whether or not it is
useful for finding bugs.  To evaluate this concern in CrashSimulator's case we
need to answer whether or not CrashSimulator's users are able to effectively
find bugs using the tool....


### Findings

Table 1 contains counts of bugs identified broken down by the tool used to
identify them and self reported developer experience level with Operating
Systems concepts. A total of !!!!15!!!! bugs were found using CrashSimulator
with the majority coming from participants with a self-reported high degree of
operating systems experience.  Participants with a moderate and low degrees of
operating systems experience found more bugs AFL.....


### Discussion

The above results indicate that, when it comes to using CrashSimulator, having
experience with operating systems concepts is very beneficial...  That said,
users with a self-reported low degree of experience with OS concepts were able
to identify bugs using CrashSimulator's built in corpus of anomalies and
checkers...  Table 2 illustrates which of these checkers were most
effective......


### Discussion on Specific Bugs

!!!Discussion!!!


## How well does CrashSimulator allow users to test the areas of applications they are interested in?

The first part of testing an application is deciding on a specific feature or
piece of functionality to evaluate.  Some appliation areas such as graphical
user interfaces are notoriously difficult cover depending on the tools and
technqiues being used.  We wanted to know whether or not CrashSimulator was able
to effectively test the areas of applications its users were interested in
testing.  To answer this question we turn to the surveys our participants
completed regarding their experience with CrashSimulator.


### Findings

The results from our surveys indicate that our participants self-reported
backgrounds have an effect on the areas of an application they tested...

Developers with a high degree of experience in software engineering tended to
focus on testing an applications interaction with various library and operating
system provided APIs.  Survery results indicate satisfied with CrashSimulator's
ability to test application's interaction with file and and network APIs....

Developers with a lower self-reported experience in software engineering focused
more on user interface level concerns...  Preferred AFL's ability to easily
supply a file to be processed to an application....


### Discussion

Findings indicate that a higher level of software development experience tends
to push participants towards testing interfaces between modules in an
application.  This resulted in overall higher satisfaction with CrashSimulator
amongst participants.....


## Does CrashSimulator allow its users to construct a test suite efficiently?

Constructing a test suite using CrashSimulator involves identifying new
anomalies to be tested for and creating the mutators and checkers required to
test an application's response to it.  There is no direct comparison to this
process in AFL...  Mutiny allows users to specify which messages should be
mutated and replayed....


### Findings

Developers reported a high degree of satisfaction with regard to the speed of
setup for AFL.  Participants felt like CrashSimulator required an overall higher
intitialy outlay of effort before testing could begin.  Additionally, they
indicated that expanding a CrashSimulator test suite by implementing new
checkers and mutators was more difficult that either expanding the scope of
fuzzing with AFL or instructing Mutiny to mutate different messages from a
recorded network session.  Participants felt that CrashSimulator allowed for
more specific testing and were pleased with the ability of CrashSimulator tests
to be used across multiple applications with minimal additional effort once they
had been constructed......

### Discussion

!!!!Discussion!!!!


## Does CrashSimulator require significant skills to be useful?

A user's background can dramatically influence their user experience with a
tool.  In answering this question we hope to ascertain whether CrashSimulator
requires its users have significant skills in a particular area in order to be
effective.  Table/Figure ZZZ compares our participants self-reported skillsets
to their positive or negative experiences with CrashSimulator...


### Findings

As can be seen in Table/Figure ZZZZ, a strong background in operating systems
concepts correlates with a more satisfactory user experience with
CrashSimulator....

Interestingly,  some participants that reported less background in operating
systems had a positive experience with CrashSimulator.  These participants
relied more heavily on built in anomalies/checkers/mutators....

### Discussion


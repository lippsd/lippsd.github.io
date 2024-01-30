---
layout: essay
type: essay
title: "Query Quirks and Answer Assembly"
# All dates must be YYYY-MM-DD format!
date: 2024-01-25
published: true
labels:
  - StackOverflow
  - Pedagogy
---
## StackinGit
Recently I was reading through the best and worst questions of StackOverflow, the internet's go-to forum for programming queries. 

Naturally, most of it was incomprehensible to me as a novice programmer with experience in but a fraction of the commonly discussed languages and technologies. 

As an interesting aside, about a third of the top 30 most upvoted questions were about Git at the time this was written, which as you may suspect from my GitHub profile (*// linked [here](https://github.com/lippsd)!*) 
I have only just started familiarizing myself with - including learning about the difference between Git and GitHub, which, FYI, is that Git is the underlying open-source version control system that GitHub serves as a web interface to.

Anyway, while I often struggled to grok the more in-depth answers given, I *was* able to get something. A few somethings, in fact. 

## \-\-> in C/C++
For one, some amusement on reading posts like, "[What is the '\-\->' operator in C/C++?](https://stackoverflow.com/questions/1642028/what-is-the-operator-in-c-c)", wherein the curious poster asks about an additional arrow operator with a double-dash (alongside the more commonly used single-dash ‘->’ operator) which inexplicably worked as ‘x down to y’ in a while loop as follows, directly borrowed from the original post:
```
#include <stdio.h>
int main()
{
    int x = 10;
    while (x --> 0) // x goes to 0
    {
        printf("%d ", x);
    }
}
```
They specifically wanted to know where it was defined in the languages' standards. It turns out that it was just an interesting quirk of how tokens are interpreted in C/C++ code, where (x --> 0) is interpreted as the condition x post-decremented is greater than 0 because white spaces are ignored. 

Beyond my own amusement, there was also an opportunity to learn about how to create good questions here. This poster concisely described a simple test case with specific inputs and outputs, the platforms on which the issue occurs, and a clear question about it - and they were rewarded with a spot in the top 10 most upvoted questions on StackOverflow, several clear answers with references to relevant standards and books, history facts... and some humorous answers comically extending the basic principle which caused the initial misunderstanding because the premise is inherently pretty silly. 

## Predictive Processing
More seriously, the question "[Why is processing a sorted array faster than processing an unsorted array?](https://stackoverflow.com/questions/11227809/why-is-processing-a-sorted-array-faster-than-processing-an-unsorted-array)", reminded me that, as valuable as big-O analysis is, it is not the be-all and end-all of practical performance. This poster noticed that a sorted array can have a portion of its elements summed up faster than the same full collection of elements in an unsorted array. They describe their attempt to understand what was going on - having built a minimum test case in two different languages with the issue consistent across both - and afterward they still had no clear idea of what was happening or why. Thus, their questions were clear: 

>"What is going on?"
>
>"Why is processing a sorted array faster than processing an unsorted array?"

The root cause was an optimization in computers called branch prediction. Essentially, computers predict what the result of a branch (if-then-else statement) will be based on past results - a sorted array has a clear pattern for the predictor to latch onto, while an unsorted array would be random enough that no pattern could be found. 

The [complete, top answer](https://stackoverflow.com/a/11227902) to this question was frankly incredible in both its readability for newer users and its depth for more experienced ones. It also goes into detail about the different ways specific compiliers optimize in situations like the one presented, and its a fascainating well-written read all around. 

The quality of this answer serves as a testament to both the quality of the question which prompted it and the universal appeal it has, since many people are likely to want to know the question's answer, and StackOverflow is designed to be a library of quality answers to programming questions as stated on their [tour](https://stackoverflow.com/tour).

## Bad Grammar Bugfix
The question "[where are the syntax errors am getting](https://stackoverflow.com/questions/30449692/where-are-the-syntax-errors-am-getting)", by contrast, serves as an example of how to not ask questions. Immediately, the grammar of the title (yes, that is exactly how it was typed) shows far less effort than the previous poster. The body of the question also includes a hefty chunk of code and a massive error chain as opposed to a minimum test case. In response, this poster received a few somewhat-explained answers - certainly nothing with anywhere near the depth of the previous example, and not something I was able to fully understand without a few rereads. The poster also received a lot of downvotes. 

In StackOverflow, downvotes actually take reputation away from both the person being downvoted *and* the person doing the downvoting. Reputation is attached to site privileges, too, so the amount of downvotes on this post speaks volumes as to the way users felt about it. 

Asking others to do what is, in my opinion, one of the least fun parts of programming - bug-fixing - is already a pretty hard ask, and the lack of appropriate grammar or politeness probably did not help. 

## Final Thoughts
My dive into the best and worst questions from StackOverflow was fascinating and I encourage others to do the same if they have some extra free time. I got to learn some history tidbits and coding quirks, but more importantly, how to ask quality questions and receive quality answers, which I absolutely need to know as a novice programmer. Hopefully, I will remember some of the lessons learned here when it comes time for me, at my wit's end, to ask a question on StackOverflow.

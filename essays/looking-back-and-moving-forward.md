---
layout: essay
type: essay
title: "Looking Back and Moving Forward"
# All dates must be YYYY-MM-DD format!
date: 2024-05-10
published: true
labels:
  - Software Engineering
  - Agile Project Management
  - Coding Standards
  - Functional Programming
---
Although I have written and thought a bunch about Software Engineering as a concept, my experience actually working with a team to design and build a complete product was nil until my work on ProfTCG.

ProfTCG is a project I completed for ICS 314 Software Engineering, a course focused on software engineering principles using web application development as a medium. 
My team and I came up with the idea while brainstorming fun applications to make for our final project, which needed to involve concepts like databases and UI.
In short, ProfTCG is a professor trading card game website which has card opening, collecting, and trading functionality - you can read more about it and what I worked on [here](proftcg.md). 

This project serves as an excellent example of the principles we have been working with all semester, and I'd like to focus in on the three principles I found most interesting: Agile Project Management, Coding Standards, and Functional Programming (// those are the labels after all!).

### Agile Project Management
Agile Project Management is a project management style which focuses on quick, iterative improvements, starting with a very rough draft / proof of concept and moving toward a finished project. 
For ProfTCG in particular, we used Issue Driven Project Management, which is a subset of Agile Project Management focusing on issues within the product that need to be solved, each assigned to available team members and completed concurrently.

I found this management style to be a double-edged sword - specifically due to the deadline schedule. 

On the one hand, the aggressive iteration involved early deadlines. These frequent deadlines forced us to complete things within a reasonable time rather than being frivolous, and as such, clear and steady progress was continually being made. 

On the other hand, these deadlines meant that a certain amount of polish was lost - decisions to solve an issue were sometimes made offhand, and since some final choice was made it would feel unreasonable to create an issue merely questioning or reconsidering something that was ostensibly completed and moved past.

Perhaps it was our inexperience within this paradigm, but regardless something was lost. It's possible that the steady progress outweighed that, though.

I can see myself more deliberately utilizing Agile Project Management in essays I write in the future. 
Although it is common to compose a rough draft and do revisions until an essay is complete, I tend to struggle with a mixture of perfectionism and procrastination when doing work like that. 
By consciously assigning myself earlier deadlines for each milestone of iterative improvement on a rough draft, I can create better products. 

The problem with this paradigm I discussed earlier would be less impactful for solo projects like an essay, since reconsidering what I have already done is something I do best.

### Coding Standards
Coding standards are self-explanatory: they are standards that code should follow, often for specific projects or teams.

The quality of my team's code, including my own, appeared to decrease as our project's final deadline approached, partly due to a lack of clear standards for us to follow. 
Our one saving grace was the ubiquitous use of [ESLint](laundering-code.md) to ensure that there was some amount of standardization between our blocks of code, pulling together our disparate snippets enough for us to keep making steady progress despite the inevitable crossovers between our issues of focus. 

Coding standards are best established at the very start of a project, as refactoring is thus not required so long as they are followed thereafter. 

In ProfTCG, the only established standard we followed was the use of ESLint. Better standards for things like commenting and documentation would have made our code collisions smoother and our teamwork stronger; when one teammate needed to work on anothers' issue, it would take a long time to adjust to the styling being used for that issue - which, obviously, felt pretty bad since we needed to make the most of our time to meet our agile deadlines.

When it comes to standards for anything - projects, code, personal boundaries, and even roommates - a firm, early establishment serves as a foundation for future success.

### Functional Programming
Functional Programming is a programming paradigm which focuses on the use of functions, which take an input and produce an output. 
In ICS 314, we focused on taking advantage of a library of functions called [Underscore.js](https://underscorejs.org/).

For the most part, I struggled to imagine the use cases of such functions. 

In my mind, it seemed that it would be best to just write a similar function up instead, well-suited to the task at hand. My inability to do so spoke to a lack of understanding in regards to JavaScript's objects and their manipulation possibilities. I thought this way up until I got stuck on a problem within ProfTCG - how do I quickly write a legible solution to the problem of taking an array of objects, isolating one value associated with a particular key for each object in the array, and then creating a new array of objects with that value being associated with two different keys?

At that point, functional programming delievered unto me the solution. Use. Underscore.

I tend to get stuck on the tiny minutiae of things. I get very particular. While this often serves me well by leading to an unusual depth of understanding, it can also make problem-solving far more difficult - I get lost in the weeds, don't see the forest for the trees, and other fun plant metaphors. 
My experiences with functional programming remind me that one of the great things about software development is that you don't (and in fact, [shouldn't](DRY-UI.md)) repeat yourself. 

Adding to that, once I have understood something with depth, such as the reasoning why a certain behavior or habit is useful, it is alright to treat the whole as a black box with simple inputs and outputs and not worry so much about the details.

### Final Thoughts
The principles I learned throughout the course of my ICS 314 course are really neat. They show how our thought processes can be honed to such a degree that they slice through problems like butter, and were made by some pretty clever people. But more than that: from social behaviors to software development, they are just plain *useful*.

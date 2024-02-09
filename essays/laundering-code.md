---
layout: essay
type: essay
title: "Laundering Code"
# All dates must be YYYY-MM-DD format!
date: 2024-02-08
published: true
labels:
  - Software Engineering
  - Coding Standards
---

Recently I have begun trying out ESLint, a linter, which enforces code quality and style checks on code as its being written. Basically, it looks at what you write and tells you that it is bad practice or outright wrong - and sometimes even why.
## What is a linter?
The term 'linter' [apparently](https://en.wikipedia.org/wiki/Lint_(software)) comes from literal laundry lint, with the analogy being that those annoying little bits of fuzz are comparable to those vague and unreadable code snippets most programmers end up writing at some point in their programming journey while steeped in a delirious haze induced by both a lack of sleep and an impending deadline.
## ESLint Experiences
So far, my personal experience with this particular linter has been less than positive. I have had to deal with a lot of annoying little configuration and setup issues which, ironically, combine into more 'lint' than could ever be present in the fairly short code snippets I write for the [Software Engineering course](javascript-and-crossfit.md) I am in. 

This almost certainly has little to do with ESLint itself. Rather, much of the problem stems from my own lack of understanding. I began using the software using tutorials that I rarely understood with any depth, making the entire setup a bit of a black box - so when something in that black box fails, its a struggle to find out why, let alone try to fix it.
## Thoughts on Linters
Regardless of my personal experiences, linters and other software that standardize code quality and style play a vital role in the software engineering ecosystem. 

In my mind, the two most significant roles standardization plays are the facilitation of teamwork and maintenance, and these roles share a common explanation. 

When new eyes - a team member, or the original creator a few days after the code was written - are looking to add more functionality to a project, standard code acts as a solid, predictable foundation. When a bug is discovered as the project is put into use, standardization allows those new eyes to follow alongside the previous programmer's intentions and ensures that each snippet is interpretable.

So long as the linter is designed well, of course.

## 

There is great gratification in finally fixing each suggestion given by a linter and getting a green checkmark. Its like the file being written [*clicked*](code-clicks.md) into completion - at least, until it runs and fails to give the desired outcome. *C'est la vie*.
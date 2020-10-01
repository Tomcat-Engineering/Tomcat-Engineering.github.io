---
layout: tip
title: Don’t use Excel for everything. Learn Python.
number: 56
tags:
 - productivity
 - tools
---

It is always tempting to use the tools you know and have to hand.  I once saw an engineer write an entire 2-d finite-element structural model in Excel, which was strangely impressive but incredibly slow and vulnerable to bugs.

Most engineers these days spend at least some of their time writing software models or analysing data files.  If this applies to you, please equip yourself with some decent tools for the job.  As a software guy, watching you lot using Excel for everything is like watching a monkey trying to undo a wheel nut using a banana.

# Why Not Excel?

- Cutting and pasting formulae across a sheet is error-prone.
- Navigating a tangle of data across loads of tabs is complicated and confusing, particularly when the tables have thousands of rows.
- Analysing data along more than one dimension is very difficult.  More than two dimensions is nearly impossible.
- Debugging is unstructured, and you can never be sure which bit is broken.
- It runs slowly if you have a lot of data.  Or refuses to work at all.
- Some things are very difficult or impossible to do.
- Repeating the analysis for another five sets of input data means creating five new spreadsheet files, and keeping them all up to date when you find a bug. 

In a programming language like Python you would structure the analysis into a set of small re-usable *functions*, each typically just a few lines of code.  You would write *unit tests* for each of the functions, which check that they give the expected outputs for a range of inputs.   You would then write a script which called the various functions for each of your input datasets.

Your functions can be re-used in future projects.   The unit tests stay with the functions, and you can automatically re-run all the tests each time you make any changes to check that you haven’t broken anything.

Python typically runs much faster than Excel, but if you need to speed things up even more there is a built-in *profiler* which tells you which lines of your code are slow so that you can optimise them.

# Why Python?

There are obviously loads of programming languages, but I recommend Python 3 for non-software engineers because it is:

- Free
- Multi-platform (Windows, Linux, Mac)
- Simple to get started
- Very popular, so lots of help and support on the internet
- Widely used for scientific work, so lots of good free libraries available
- An interpreted language (runs immediately without having to compile it first)
- A high-level language (meaning you write fewer lines of code and don’t need to worry about memory management etc.)
- Mostly fairly intuitive.  At least it is to me, but I’m a programmer…
- A decent programming language, widely used by real software engineers.  For basic engineering analysis you are unlikely to outgrow it.

# Software Engineering Tools

There is also another set of problems which non-software engineers encounter when they write software (in Excel):

- Keeping track of what changed when can be a nightmare, particularly when there is more than one person involved.  You typically see loads of different versions of a file saved with increasingly long and cryptic filenames.   Sometimes your version diverges from somebody else’s version.  Sometimes you can’t reproduce important results.
- It is tricky to re-use code.  Working code snippets get pasted between files, but if you discover a bug then who knows how many other files are affected?  Was the snippet actually designed for your scenario, or does it actually not work correctly for negative numbers?
- People almost never make use of third-party code, so end up solving common problems from scratch.  If they do use third party code, it is just pasted in off the internet so won’t get updated when the original author finds a bug.

Luckily software engineers solved all these problems decades ago – you just need a version control system with a central code repository.  This may sound daunting but you could set this up in ten minutes ~~if you are willing to pay Github $25/month~~ and [Github](https://github.com) is now free even for private repositories!  

---
layout: project
type: project
image: 
title: Squibbish
permalink: projects/squibbish
# All dates must be YYYY-MM-DD format!
date: 2017-06-01
labels:
  - Kotlin
  - Bash
  - Language implementation
summary: A small transpiled language, written from scratch
---

`Squibbish` was one of my hobby projects from 2017. I write a lot of system scripts, and at one point I had gotten frustrated over the boilerplate and weak typing that comes with writing in bash. I decided that I'd need a new scripting language that had slightly more structure. In general I don't advocate for reinventing the wheel (and eventually I did land on using python), but I thought that this would be a good opportunity to try out some of the compiler techniques that I had been reading about at that time. 

Around 2017, I was still working on figuring out some of the more advanced language features that kotlin had to offer. In Jetbrain's YouTrack board, there was a lot of discussion being done on how improvements could be made, and it got me interested on what actually went into writing a brand new language. To hone my kotlin scripts, I decided to write the transpiler in Kotlin - and to make the project easier, I decided to output the code directly as bash. 

For those that are interested, I recommend [the purple dragon book](https://en.wikipedia.org/wiki/Compilers:_Principles,_Techniques,_and_Tools) for learning compilation techniques.

I went down a rabbit hole almost immediately with grammar parsers. Bison/Yacc/ANTLR and similar parsers did not fit my needs - they required C/ASM code and they had a lot of legacy considerations that made their API hard to use. I would consider them for an enterprise grade language, but not for a toy language which was intended to improve my kotlin skills!

One of the first lessons I learned when starting again from scratch was that test driven development (TDD) is a must when writing compilers. When starting out, it is a good idea to start with the basics like comments and print statements, but introducing parsing of control flow statements can cause chaos in your output. Being able to run tests consistently after small changes meant that I was able to make incremental progress while ensuring that I was not breaking previously stable functionality. 

One of the nice perks of this was that I was able to write the source code that I wanted first, and use the test to generate some transpiled code as an execution candidate. When I ran the snippet, I would be able to validate the output, and if it was completely correct, it would become the "expect" case for the assertions in my tests. 

Ultimately, I think I got a lot out of the project. I have a deeper understanding of what it takes to write a language, I improved quite a bit in my kotlin skills, and I have a cool language project that fits my own aesthetic for code. 
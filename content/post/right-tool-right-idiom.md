---
title: "The Right Tool, The Right Idiom"
date: 2022-06-13
author: "Howard"
draft: false
description: "As more and more traditionally-trained developers have migrated into the Javascript space, I've seen quite a few attempts to bring across idioms, patterns, and even and tools commonly found in large OO code bases. Some of those things have made their way into the core language itself and some have caused the creation of new languages. Nearly all of these examples illustrate the application one tool chain's idioms onto another - and in many of the above examples, the result is unintentional and unnecessary complexity."
image: ""
tags: ["architecture", "javascript"]
URL: "/2022/06/13/right-tool-right-idiom/"
---

Jeff Atwood, the co-founder of Stack Overflow and developer who famously said "Any application that can be written in JavaScript, will eventually be written in JavaScript" wrote a post back in 2005 entitled ["You Can Write FORTRAN in any Language"](https://blog.codinghorror.com/you-can-write-fortran-in-any-language/). At the time, Microsoft's .NET framework was relatively new, and there were lots of heated discussions around a new programming language, C# and what it meant that so many Visual Basic programmers were dropping VB [with prejudice](https://www.law.cornell.edu/wex/with_prejudice) in favor of it.

Now, I'm not going to wade back into the core substance of Jeff's article and the Microsoft language wars of the early 2000s because some of those scars are still healing. However, the post triggered a thought that's been brewing for a while - especially as I've watched the evolution of Javascript applications over the last few years. Consider the following.

> Today, any Java-related google query will return reams of truly mediocre "explosion at the Pattern Factory" Java code. All I can say is, __enjoy [the newness of C#] while it lasts__.

So what does this have to do with anything happening almost 20 years ahead of when that post was written - and what does FORTRAN have to do with Javascript?? 

It comes down to the relationship between tools and idioms. 

As more and more traditionally-trained developers have migrated into the Javascript space (thanks a lot, Node!), I've seen quite a few attempts to bring across idioms, patterns, and even and tools commonly found in large OO code bases (e.g. C# or Java). A few examples include dependency injection containers, mocking frameworks, DTOs, and ORMs. Some of those things have made their way into the core language itself (e.g. classes), and some have caused the creation of new languages that get cross-compiled into Javascript (e.g. TypeScript). Nearly all of these examples illustrate the application one tool chain's idioms onto another - and in many of the above examples, the result is unintentional and unnecessary complexity. 

I'm sure that there are as many reasons as there are developers, but one that I've heard and seen frequently when it comes to Javascript projects looking like Java projects is the expectation of project size. If you've worked in a typical enterprise development environment, you're undoubtedly familiar with incredibly large Java or .NET projects which are nearly impossible to manage without complex integrated design environments (IDEs) that can do super cool things like deeply integrate with a [strongly-typed] language's type system to provide discoverability, intellisense, and automated refactoring tools.

Here's the thing though - As you're probably painfully aware, Javascript (and other loosely-typed languages) was never really meant for and is generally not very good for managing really large projects. In fact, most of the core language features (ya know, [the good parts](https://www.amazon.com/JavaScript-Good-Parts-Douglas-Crockford/dp/0596517742)) came from 2 other languages also not really meant for super-large enterprise projects: [self](https://selflanguage.org/) and [scheme](https://groups.csail.mit.edu/mac/projects/scheme/). Examples include first-class functions and a limited set of simple data structures such as arrays and objects. As such, idiomatic Javascript, in my view, is really oriented around creating small components/projects. This is one reason why I think it lends itself so nicely to architectures that make use of functions as a service (FaaS). If you're implementing patterns in Javascript such as DTOs so that your IDE can do nifty code completions so that you can then manage a large Javascript project, you may be in the middle of creating a self-fulfilling prophecy. 

So to sum it up, I want to expand a bit on one of my core engineering principles. Use the right tool for the right job, but use the intended idioms for that tool.

Just something to think about :) 

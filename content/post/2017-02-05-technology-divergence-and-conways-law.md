---
title: "Technology Divergence and Conway's Law"
date: 2017-02-05
author: "Howard"
draft: false
description: "Conway's law is an observation that \"Any organization that designs a system (defined broadly) will produce a design whose structure is a copy of the organization's communication structure\". As a developer, it's easy to believe that this dynamic is the result of management decisions - however, sometimes the reality is more nuanced."
image: "/images/divergence.jpg"
tags: ["architecture", "management"]
URL: "/2017/02/05/technology-divergence-and-conway-s-law/"
---

In 2015-2016, there was a fair amount of discussion in the industry about the rise of polyglot development. The idea was simple enough: rather than standardizing on a set of programming languages and tools, development organizations would choose the right tool for the right job. Successful developer in this brave new world needed then to learn a host of new tools, from languages and frameworks like NodeJS, Golang, Elixir, and Rust to infrastructure automation tools like [Docker](https://www.docker.com/), [Mesos](http://mesos.apache.org/), [Terraform](https://www.terraform.io/) and beyond.

I have and continue to have a great deal of pride in the people that I bring into my development teams. They are, in my clearly biased opinion, the perfect blend of intelligent, curious, and driven. As a result, they were more than happy to apply the polyglot mantra to the services that they built - even when those choices diverged significantly from those of the rest of the company (both other development teams and central infrastructure teams). And those resulting services have performed exceptionally well in terms of all relevant technical measures. The team has also been able to successfully operate their own services in a truly end-to-end fashion. On the surface, the promise of polyglot development would seem to live up to all that it promised.

The real challenge of polyglotism and technical divergence didn't really materialize until we wanted to hand off one of our projects to another development team in the company. When planning out how me might do this, we quickly realized that nearly _everthing_ we did, from the code we wrote to the method in which we deployed, to even the infrastructure on which we ran, was different from that of the team to which we wanted to transfer project ownership.

The challenge of moving projects between teams because of technical divergence sparked some interesting conversation within the team related to the often-cited [Conway's law](http://www.melconway.com/Home/Conways_Law.html). This observation states (paraphrasing) that a system will end up looking remarkably similar to the structure of the organization that produces it. Often, as developers, we easily find the observation to hold true, but are comfortable in assuming that the organizational structure is created by disconnected or incompetent managers pursuing their own selfish agendas at the expense of innocent [and brilliant, of course] developers.

But what if, as we were experiencing, Conway's law could actually be a function of technical choices made by the development teams themselves? What if, by venturing so far outside the company's technological norms and competencies, we had put ourselves in a position where the project could not actually be transferred to another team? Should this prove true, and should it happen across a set of projects, project ownership would become stagnant and brittle, thereby preventing technology from being able to adapt to change in tandem with the business.

Put more simply, divergent technology choices could in fact cause Conway's law.

So should we then just all standardize on Java and call it a day? While this strategy may be able to avoid the dynamic described above, it would yield the side-effect of stifling innovation, which is also not desirable for a business. The happy path must lie somewhere in the middle. And while I don't yet know in an absolute sense what that path looks like, here are the three actions that I'm currently taking to try and find it.

1. Look for opportunities to converge with the company on technology. One of the successful aspects of our diverging was that demonstrated value in different technology components and methods, and insodoing helped to move the company forward in innovation. We are now looking for ways to adopt the company-"standard" implementations of those components.
1. Work with the leadership of different groups - particularly centralized operations groups - to define a path by which we can diverge, influence, and converge in a repeatable and agile cadence. Following the same principle as code branching, the longer you build isolation, the more painful it is to merge. In the future, we hope to be able to "merge" much more quickly and painlessly than we are currently experiencing.
1. Have a more serialized approach to influence. In addition to the amount of time that we diverged, the fact that we diverged in almost every technology area imaginable has also been a major barrier to convergence. Going forward, we will be more strategic about what we want to influence, and then focus on that area until it is resolved.

At the end of the day, I'm finding that for a company of our size and breadth, the ability to preserve fluidity of projects across the  development organization is more important than being the most forward-thinking in all areas of technology. Without it, Conway's law seems unavoidable - with or without those self-serving managers :)

---
title: "Kicking the Tires with GitHub Actions"
date: 2022-08-30
author: "Howard"
draft: false
description: "As components break down into smaller units, more dependencies between those components means I need more rigor in producing them. I've been following the progress of GitHub Actions since it was first announced, but hadn't actually tried using it until now."
image: ""
tags: ["continuous integration", "GitHub actions", "tools"]
URL: "/2022/08/30/kicking-tires-github-actions/"
---

In my side-life, I'm working on developing a backend and reference architecture for a lightweight, reactive, RDF-based architecture, and as things go - particularly in NodeJS applications - clearer understanding of component usage caused me to want to refactor larger components into smaller ones. This componentization meant that I now had the need to manage Node package dependencies between my own components, and while just referencing the Git repository directly worked for a period of time, as the number of components grew, it became clear to me that additional rigor was needed. 

In the past, [I've used a bunch of different job runners](http://localhost:1313/2015/03/13/our-development-pipeline-and-process/), from the one everyone loves to hate - Jenkins - to Circle CI (and other Travis CI-inspired SaaS tools) and most recently, GitLab. To be honest, they're all fine - and they all have their own little irritations. I find GitLab in particular to be pretty powerful, but downright cryptic for some use cases. I knew that GitHub had built a runner quite some time ago, and I've had friends that have both worked on its development and created content teaching others how to use it, so when the need arose to add some automation to my work, it seemed like a great idea to try it.

I'll write more on my learnings as I get deeper into it, but here are a couple high level reactions so far.

* The actions marketplace is really slick. In GitLab, extended capabilities come in via runner base images or referencing scripts that someone else created, but the explicit, discoverable, versionable actions as really lovely to work with
* While I saw that there is a repository for reference workflows, I still don't have a completely clear picture of how to structure mine such that
	* tests are run on every commit (or should they just be run on every PR?)
	* node `package.json` version is bumped on every merge into main
	* the package is published to GitHub's package repository on every merge into main
	* should a GitHub release be created?
	* code coverage and test reports should be published and made available
	* JS Doc files should be built

I'm sure I'll figure this out and I'm sure it's probably much simpler than I'm making it out to be right now. So far though, I'm really liking what I'm seeing.

Now, on to pushing this commit so that my [blog automatically builds and pushes to Firebase](https://github.com/howarddierking/www.howarddierking.com/blob/main/.github/workflows/main.yml) :)
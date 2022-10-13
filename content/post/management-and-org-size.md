---
title: "Management: Organization Size May Not Be As Important As You Think"
date: 2022-10-12
author: "Howard"
draft: false
description: "I recently interviewed with a company who was looking for a senior engineering leader, and the conversation took a surprising turn, so I want to take a few minutes with you good folks and think about what makes a manager qualified to build or lead an organization of a certain size."
image: ""
tags: ["management"]
URL: "/2022/10/12/management-and-org-size/"
katex: true
---

I recently interviewed with a company who was looking for a senior engineering leader, and the conversation took a surprising turn related to management and organization size, so I want to take a few minutes with you good folks and comment on the following question:

> Is organization size a useful measure in predicting whether a new or potential manager will be successful? 

## The Context

First, here's the context behind this post. In the course of an introductory conversation with the company recruiter, I was asked what was the largest team I had managed. When I responded with \~110-120, the recruiter promptly ended the interview, saying that they wanted to find someone who had experience managing a team of around 200. This response startled me a bit because honestly, it's the first time this particular issue has ever come up - let alone was a conversation-ender. But at the end of the day, it's the company's choice to make, so I thanked the recruiter for their time and we ended the call.

Fast forward an hour or so and I still couldn't get it out of my head why _that_ particular issue was such a central measure in the company's recruiting process. Intuitively, organizational size seemed like such an odd metric, disconnected from any specific organizational goals, structure, or management philosophy - especially considering that in the course of the conversation, the recruiter had shared how they have an existing management structure consisting of 3 levels (2 levels of management). Like I said, it just seemed "off" for lack of a better term.

## The Problem 

In thinking about it more, I realized that the circle I was trying to square was related to a topic that I dealt with fairly recently when making some organizational design changes. That topic is [span of control](https://en.wikipedia.org/wiki/Span_of_control). Further, I realized that what was driving my response was remembering just how large the organizational size range can be when combining span-of-control with organizational depth.

So, like any good nerdy type, I went to Excel to put some numbers to my intuition. If we play with different values for depth of management and span-of-control, you can see that we end up with some pretty large numbers pretty quickly for the max supported organization size.

| levels of management | span of control | max org size | notes |
| -------------------- | --------------- | ------------ | ----- |
| 2 | 4 | 20 | assumes levels: manager / IC |
| 2 | 5 | 30 |  |
| 2 | 6 | 42 |  |
| 2 | 7 | 56 |  |
| 3 | 4 | 84 | assumes levels: director / manager / IC |
| 3 | 5 | 155 |  |
| 3 | 6 | 258 |  |
| 3 | 7 | 399 |  |
| 4 | 4 | 340 | assumes levels: director / sr manager / manager / IC |
| 4 | 5 | 780 |  |
| 4 | 6 | 1554 |  |
| 4 | 7 | 2800 |  |

If we want to have more fun with this, we can also calculate max organization size with the following summation: 

* let `l` = levels of management
* let `s` = span of control

$$\sum_{i=1}^l s^i$$

## A Different Approach

From looking at the data, my conclusion validated my intuition: unless an organizational structure is completely flat (e.g. everyone reports to a single individual), size is not a terribly informative measure when it comes to assessing whether an individual has the requisite background to manage the group. To borrow from the sage wisdom of software developers through the ages: "it depends".

So to conclude, for those of you out there charged with recruiting and assessing managers, I would like to offer up this thought for you to consider. Ensure that the measures you choose in your evaluation align with both your company goals and your organizational structure. If you want an individual capable of large scale org design and reorganization, look specifically for those experiences. If you're happy with the current depth and span-of-control mix, ensure that the individual has operated in those environments.

If you over-index on the wrong measure - as I believe was the case in this instance - you will in a best case overlook strong candidates, and in a worst case hire an individual who may be exceptional at building large empires and little else.
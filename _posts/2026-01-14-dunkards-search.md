---
layout: post
title: "Drunkard's search"
date: 2026-01-14
---

A policeman sees a drunk man crawling on his knees under a streetlight and approaches him:
- What are you doing?
- I’m looking for my keys
- Did you lose them here?
- No, I lost them in the park across the street but the light is much better here!

When measuring effectiveness of their tech teams, non-tech organizations tend to focus on things they can see: 
 * did we meet the deadline?
 * were we on budget?
 * how many bugs did customers report?

There are two problems with these metrics:
 1. they lag. You only see them when it's already too late (your key is already lost in the dark): the code is too complex or buggy, teams are already exhausted chasing deadlines.
 2. they don't measure the underlying problem: how hard is your codebase to understand and modify? Let's call this software modifiability. Some also call this cost of change.

Measuring modifiability of your system is hard because it goes beyond just code complexity - it also includes integration and deployment pipelines, your testing procedures, your production observability. 

DORA metrics are a decent attempt of going one step deeper: the four key metrics (Change Failure Rate, Lead time to Change, Deployment Frequency, Mean time to Restore) try to capture exactly these aspects of your code modifiability. 

We could go further, showing engineers relevant proxy metrics they can act on in their PR (code complexity, code coverage, PR size, etc). This could then aggregate and provide a nice pyramid-like view across the board. 

From metrics non-tech people care about (delivery predictability, uptime, customer complaints), through DORA metrics, all the way to code complexity, pipeline runtime metrics, and even production performance metrics individual teams and engineers will directly be able to act on.

This is clearly a lot of work and unlikely to be plug-and-play, but I think we should be able to connect the golden thread across layers of the pyramid. 

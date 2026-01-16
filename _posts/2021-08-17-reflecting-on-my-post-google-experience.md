
---
layout: post
title: "Reflecting on my post-Google experience so far"
date: 2021-08-17
---

TL;DR I left Google two years ago to join Superbet, a rapidly growing European sports betting business. I first discuss why I made the call, share a bit of what I learned about betting, and finally reflect on my experience so far.

## Let’s first address the elephant in the room

Betting is still taboo in most of the world, so I had to do some introspection whether I wanted to be a part of that world. On one hand, most human activity has side effects (aka externalities) so it’s easy to dismiss gambling as being yet another business with negative externalities. On the other hand, I didn’t want to dismiss these externalities without exploring them deeper.

As with most values-based decisions, this is primarily a personal question so I don’t think my judgement can be universally applied, but my thought process might resonate with some, so I thought it worth sharing. I realized that I wouldn’t have qualms working in other industries with significant negative externalities such as the oil & gas or the auto industry, alcohol producers, the pharma industry, or the tech giants. Most societies today don’t do a great job of compensating the negative externalities of these industries, but the situation is improving — our cars are greener, alcoholism treatment and awareness is increasingly available, and even big tech is getting closer scrutiny these days.

Betting and gambling is heavily regulated and taxed, with increasingly strict responsible gambling rules and limits. So how big of a problem is problematic gambling? [This Wikipedia article](https://en.wikipedia.org/wiki/Problem_gambling#Europe) suggests roughly 0.5–1% of the population exhibits problematic gambling behaviour. [This survey](https://www.imedpub.com/articles/incidence-of-problem-gambling-inromania-brief-report.php?aid=18557) puts the number for Romania (Superbet’s home turf) around 0.6%. Alcoholics account for around 5% of the population according to [this other Wikipedia article](https://en.wikipedia.org/wiki/Alcoholism#Epidemiology).

Given that preventing access to gambling for problematic players is not only doable, but mandated by law and increasingly strictly regulated, I decided I’m fine with making the call.

## Betting Software Ecosystem is surprisingly complex

The first thing that overwhelmed me when I joined was the sheer complexity of sports betting, so thought it might be useful to shed some light on that. The basic idea of a betting business is one of mediation — in an ideal scenario the betting operator is just an intermediary between two punters who want to bet on the same event. The odds reflect demand/supply for each of the outcomes, minus the operator’s margin.

In practice, you don’t always live in an ideal scenario (e.g. the event is not prominent so supply or demand are not liquid enough), so providing a smooth betting experience regardless is harder than I expected. Also, the distribution of customer interest for betting events is a power law, making for very spiky customer traffic patterns.

The software ecosystem dealing with all this complexity can be organized in three major product areas:

 * Trading side: this is the part of the ecosystem that ingests sports and betting market data and builds the betting offer through offer management and risk tooling. A 100+ people ops team (called traders because determining the odds is essentially a supply/demand problem) use these tools to make sure Superbet has the broadest, deepest, and best priced betting offer on the market.
A Google Search equivalent of this would roughly be Indexing.
 * Betting side: the transactional, customer-facing part of the system, that includes the betting clients apps and the systems enabling the betting ticket lifecycle.
This roughly corresponds to Serving in Search.
 * Operations side: running a multi-channel, multi-country business of this scale requires a lot of operations support tooling that enable us to operate the retail betting shop network, customer support issues, marketing and CRM ops, etc. 

## My experience so far

While our DAU or QPS metrics are nowhere near Google scale, the complexity of problems being solved is comparable, especially when you take into account that you have to do a lot of things from scratch, without relying on the massive Google infrastructure.

The main thing I loved about my new team was how easy it was to try out new things — ideas, tools, processes, or ways of working. While Google is probably reasonably fast for its size, this is just in a different ballpark. We talk about something, decide to try it, and start doing it next week.

While nimbleness of a smaller team is inspiring, some things just work much better at scale. Most Googlers don’t have to know how to configure or manage a Borg cell, distributed in-memory cache, or a large database system correctly. If you solve the quota issues, you can count on the system working without knowing a lot of internal SRE magic (modulo the occasional cell deprecation or maintenance ;-) ).

We mostly had to figure these things out on our own and learn way more details than we planned to. This doesn’t only apply to engineering practices. We also had to figure out how an engineering career ladder should look like, introduce design docs and postmortems, figure out oncall and escalation procedures, quota planning, etc.

My initial thinking was to just do it the Google way but we quickly learned that while most of Google’s ideas are generally applicable, the devil really is in the details, and there’s no one-size-fits-all approach that works across organizations of different sizes, different cultures, and industries.

## So, what’s next?

It is a cliche, but things are just getting interesting. On the one hand, Superbet is expanding its operations geographically, providing a steady stream of localization, integration, and migration challenges. On the other, we have a ton of exciting product ideas we want to try out.

We see ourselves as primarily a tech company working in the betting industry, rather than a betting company. That puts us in a position where due to the heavy investment in our software ecosystem we can try out new product ideas and pivot as we learn more. This is an industry dominated by major players using off the shelf b2b solutions, so we think fully owning the whole customer experience is our long term competitive advantage.

Our next big organizational change is the pivot towards self-sufficient and empowered product teams. This will open a lot of interesting engineering challenges. For example, it’ll be crucial to figure out how to build platforms that are easy to contribute to, yet rock solid in terms of stability and performance. Product teams will also require a mindset shift; encouraging engineers to get actively involved in feature discovery, hypothesis testing, and delivery is radically different than what they’re used to.

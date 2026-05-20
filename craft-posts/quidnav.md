---
title: QuidNav
slug: quidnav
type: project
date: 2025-01-01
tags: [product, saas, next.js, supabase, open-source, fintech]
project: quidnav
---

# QuidNav

## The Brief

QuidNav started as a personal frustration turned public resource. Personal finance in the UK is either buried in jargon, hidden behind paywalls, or scattered across subreddits, YouTube channels, and book recommendations passed between friends. There's no central place to find the good stuff — and most people never start their financial journey at all because nobody hands them the map.

The spark was a book recommendation. A friend suggested *How to Own the World* by Andrew Craig — plain English, no jargon, just the fundamentals of making money work for you. It landed. And from that point, the reading list grew, the podcasts stacked up, the subreddits multiplied. At some point it became obvious: this journey only started because of a single recommendation. Most people never get that recommendation. QuidNav was built to be it.

## The Problem

Personal finance is a taboo subject in the UK. People don't talk about money. They don't teach it in schools. And when someone finally decides to take it seriously, they face a wall of noise — conflicting advice, products dressed up as education, and resources built for the US market that barely apply here.

The statistic that stuck: roughly one in four UK families couldn't survive a month without a paycheck. Not because people are careless — but because nobody ever showed them how money actually works. The complexity is largely manufactured. Scratch beneath the surface and it isn't that hard. You just need the right resources and the right starting point.

That's the gap QuidNav exists to fill.

## The Approach

The decision to build it as a community-driven database rather than a curated editorial site was deliberate. No single person should be the authority on what's useful — the community should surface that through use. Resources submitted, reviewed, and ranked by the people who found them genuinely helpful. The best ones rise. The noise falls away.

It was built open source from the start and structured as a non-profit in spirit — any revenue purely to cover running costs, never to extract value from people trying to learn. Free to use, free to contribute, free to benefit from.

The design philosophy matched the mission: get out of the way. One page. A search bar. Find what you need and go learn. No dark patterns, no upsells, no manufactured complexity.

## The Work

QuidNav is a single-page resource database built on the MM stack — Next.js, TypeScript, Tailwind, Supabase, Resend. The interface surfaces the full database immediately, filterable by media type, topic, pricing, and platform. The search is intentionally conversational — users can describe what they're looking for in plain terms ("podcasts about pensions I can listen to in the car") and the search returns relevant results rather than forcing keyword matching.

Each resource has its own breakdown: what it covers, which personal finance topics it touches, where to access it. Community accounts allow resource submission, which goes through manual review before entering the database. Upvoting and downvoting is built into the roadmap — the mechanics are designed, the implementation is next.

The project is fully open source. Donations are the only revenue mechanism, and only ever to keep the lights on.

## The Outcome

QuidNav is live at quidnav.com and growing its database. It's a passion project that hasn't yet had the sustained attention it deserves — the vision is bigger than the current build. But the foundation is solid, the architecture is right, and the mission hasn't changed.

The roadmap is clear: community voting, AI-assisted resource discovery, free financial guidance, and eventually a genuine hub that finance creators and educators point people toward as a starting place. A gateway, not a destination. Something spoken about in the same breath as the resources it recommends.

It's unfinished in the best way. The bones are good. It just needs the love.

## Stack & Tools

- **Next.js** — framework
- **TypeScript** — type safety throughout
- **Tailwind CSS** — styling
- **Supabase** — database and auth
- **Vercel** — deployment and hosting
- **Resend** — email delivery

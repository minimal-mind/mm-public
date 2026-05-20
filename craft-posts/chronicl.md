---
title: Chronicl
slug: chronicl
type: project
date: 2025-01-01
tags: [open-source, developer-tooling, ai, documentation, practice, context]
project: chronicl
---

# Chronicl

## The Brief

Codebases have narrative. Decisions get made in meetings that never make it into the code. Design choices get debated in Notion, in Slack, in conversations between engineers — and then disappear the moment someone new joins the team, or an AI agent opens the repo for the first time.

Chronicl is a development practice, not a product. A lightweight markdown convention for adding narrative to your codebase — capturing the decisions, the reasoning, the deliberate choices and deliberate rejections that shape how a project is built. For humans and AI alike.

## The Problem

Managing a development team at the dawn of AI-assisted coding made one thing obvious: AI agents were being treated like another developer on the team, but without any of the context a real developer accumulates over time.

The context gap has two sides. Outside the IDE, real project decisions happen in meetings, calls, and documents — design choices get debated and revised without leaving any trace in the codebase. Inside the IDE, developers make hundreds of micro-decisions while coding — naming conventions, library preferences, performance trade-offs, security considerations — that happen instinctively and almost never get written down.

The result: an AI agent suggests a package you've deliberately avoided for security reasons. It recommends a pattern that contradicts a design decision made three sprints ago. It has no way of knowing what the codebase is actually for, what it's trying to avoid, or where it's going. Every new session starts from scratch.

The same problem applies to new team members. And to the developer themselves, returning to a codebase after six weeks away.

Codebases are never static. They evolve, they grow, they change direction. Some decisions are made in stone. Others get revisited. All of it is narrative — and almost none of it gets captured.

## The Approach

The solution had to be lightweight. It had to be readable by both humans and AI without any tooling or setup. It had to live inside the repository itself, version-controlled alongside the code it describes. And it had to be structured enough to be useful without being so rigid that it became a burden.

Markdown was the only answer. A single file — `chronicl.md` — placed at the root of the repository. A template with defined sections: overview, motivation, tech stack, design decisions, risks, open questions, next steps, and a dated journal.

The journal is the core. As developers work — making decisions, hitting obstacles, changing direction, completing features — they add dated entries. The codebase accumulates a timeline of its own development. The reasoning behind every significant choice lives alongside the choice itself. An AI agent, a new team member, or the original developer returning after months away can open `chronicl.md` and understand not just what was built, but why.

Inspired by `llms.txt`, Cursor Rules, and the broader movement toward giving AI agents better context — but opinionated about structure, and built around the journal as the primary mechanism.

## The Work

A practice. A template. A README that explains both.

The `chronicl.md` template covers: codebase overview, motivation and objectives, tech stack, contributors, design decisions, risks, open questions, next steps, ad-hoc notes, and a dated journal. Sections are non-mandatory — the practice scales to the team and project — but the recommendation is to have at minimum an overview, motivation, risks, and a living journal.

The workflow is simple: start with the template, update as you work, journal each branch or feature, review before merging. Over time the file becomes the institutional memory of the project.

It's been adopted internally across every MM codebase and made a formal part of the development process. Mercury's repo has a `chronicl.md`. The practice works — it catches context that would otherwise disappear, keeps developers aligned with the original goals of the project, and gives AI agents something to actually reason with.

## The Outcome

Chronicl hasn't gone viral. It doesn't need to. It's an opinionated practice released into the open source world alongside things like `claude.md` and `agents.md` — contributions to the conversation about how developers and AI agents should share context. Whether it catches is for the industry to decide.

What it does is work. Every codebase that runs it has a narrative. Every AI agent that reads it has context. Every developer who opens it after a long absence knows where they are.

That's enough.

## Stack & Tools

- **Markdown** — the entire point
- **GitHub** — home and distribution
- **MIT License** — open to all

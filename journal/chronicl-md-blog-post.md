# chronicl - your codebases story

Most documentation tells you what the code does.

Almost none of it tells you why.

Why is the part that matters. For your team. For your future self. For the AI tools now sitting next to you in every editor.

chronicl exists to close that gap. Not a file. A habit. And we think it's bigger than one project — it's an idea the whole industry could use.

---

## Where it started

The idea came from running teams and shipping software. Decisions happened in meetings, in Slack, mid pair-programming session. Then they vanished. Nobody wrote them down. So every new feature came with the same questions:

- Why was this built this way?
- What did we trade off?
- Why not the usual library?
- What was the context nobody remembers?

The AI tools had it worse. They weren't just out of the loop — they didn't know a loop existed. New session, same rejected pattern, suggested again with total confidence.

That friction adds up fast.

---

## The name is the point

Not documentation. A story. The record of how a thing came to be - he decisions, the dead ends, the reasoning that never survives a Slack thread.

Code tells you the ending. chronicl tells you how you got there.

---

## The Context Gap
AI coding assistants struggle with two critical blind spots:

Outside the IDE: Real project decisions happen in meetings, chats, and conversations—design choices get debated and revised without leaving a trace. Your AI assistant misses this crucial context.

Inside the IDE: When you're coding, you make hundreds of micro-decisions—naming conventions, helper methods, library choices, performance trade-offs. These happen instinctively and rarely get documented.

The result? Your AI assistant suggests patterns that clash with your design intent, recommends libraries you've deliberately avoided, or misses performance considerations you've already addressed. Each new session forces you to re-explain everything from scratch

---

## What it looks like in practice

Teams run AGENTS.md and CLAUDE.md already however what's captured in these files isn't the whole story. 

These tend to capture code preferences:
- This is how we write tests
- We prefer to place assets here
- Always use colours specified from globals.css

However, this is only a piece of the story. 

It's like watching Bilbo Baggins run from orcs to get to the Lonely Mountain without knowing he started this journey started in the Shire to help the Dwarfs reclaim their home.

This scene would mean nothing to you without knowing the whole story - this is what Chronicl achieves and as it lives with the codebase on every pull each of your team is reading from the same story. 

As you meet, code, chat, commit, PR this doc is here to capture that into chronicl. 

### Examples

- You see that Fable 5 has spotted a new CVE in a npm package so you decide as a team in your daily stand up you won't use that package. Noone told your agents so they still implement this package when you develop a feature.
- Your senior dev implemented a standard and sent a Slack message detailing it - 2 people read it, your agent couldn't. The team build features with old standards in place resulting in refactoring later.
- Your tech stack UV for Python package management but your agents still importing packages using PIP - Same for npm and pnpm

---

## What a chronicl file holds

One markdown file, at the root of your repo. Part journal, part architecture guide.

A solid one usually covers:

- **Overview** — what this is, who it's for, what it solves
- **Motivation** — the why behind the build
- **Tech stack** — what you chose, and why
- **Design decisions** — trade-offs, forks in the road, roads not taken
- **Risks** — the stuff that could bite you later
- **Notes** — standup thoughts, half-formed ideas, peer input
- **Journal** — dated log, branch by branch, feature by feature

Minimum viable version: Overview, Motivation, Risks, Journal. Everything else is upside.

---

## Who it's for

**Teams**
Tribal knowledge stops leaving with people. Onboarding gets faster. Every agent in the stack works from the same context instead of guessing at it fresh each time.

**Solo builders**
You stop re-solving problems you already solved. Your AI gets sharper session over session. And you end up with an actual archive of how the thing was built — not just what it became.

---

## Not the first to think this

chronicl didn't arrive from nowhere. It sits alongside a few related ideas already doing the rounds:

- **llms.txt** — a human-readable primer for AI on your repo
- **Telos** — structured narrative built for LLMs
- **CLAUDE.md / AGENTS.md** — persistent context loaded at the start of a session
- **Cursor's rules** — persistent context baked into the workflow

The difference: chronicl isn't a config file. It's a story your project tells about itself — one any agent, or any new hire, can pick up and read.

---

## The workflow

1. Start with the template. Fill in the basics.
2. Log as decisions happen. A bullet point takes ten seconds.
3. Journal regularly — one entry per branch or feature is a good rhythm.
4. Review before merging. Keep it current, not cluttered.
5. Adapt it. It's your file.

---

## Why we think this matters for everyone

For humans: clarity, ownership, a shared source of truth.

For AI: memory that survives the session, not just the prompt.

For the project: a record that actually means something six months from now.

This isn't just how we work at Minimal Mind. It's the practice we think teams — and the tools they build with — are going to need more of, not less.

---

## Try it

Start with three sections. Ten minutes, tops.

The value isn't in the setup. It's in the entries you keep adding.

→ [Read the docs](https://chronicl.dev)

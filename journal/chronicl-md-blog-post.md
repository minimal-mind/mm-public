# chronicl.md — giving your codebase a voice

Most documentation tells you what the code does.

Almost none of it tells you why.

Why is the part that matters. For your team. For your future self. For the AI tools now sitting next to you in every editor.

chronicl.md exists to close that gap. Not a file. A habit.

---

## Where it started

The idea came from 14IP, leading a team on internal automation and APIs.

Decisions happened in meetings, in Slack, mid pair-programming session. Then they vanished. Nobody wrote them down. So every new feature came with the same questions:

- Why was this built this way?
- What did we trade off?
- Why not the usual library?
- What was the context nobody remembers?

The AI tools had it worse. They weren't just out of the loop — they didn't know a loop existed. New branch, same rejected pattern, suggested again with total confidence.

That friction adds up fast.

---

## The solo version of the same problem

At Minimal Mind, working alone, the problem doesn't disappear. It just changes shape.

Solo, you hold all the context. Your AI holds none of it. And eventually, neither do you.

I was already keeping notes.md files — scattered, inconsistent, useless to anything but me on a good day. Not exactly a system.

So I built one.

A lightweight file that evolves with the project. Something a human can follow. Something an AI can actually use. Something I'd keep up, because keeping it up is the entire point.

---

## What chronicl.md actually is

One markdown file, at the root of your repo. Part journal, part architecture guide.

It holds your decisions, your reasoning, your project's shape over time — so context is something you build, not something you lose.

A solid chronicl.md usually covers:

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
Tribal knowledge stops leaving with people. Onboarding gets faster. AI tools get consistent context instead of guesswork.

**Solo builders**
You stop re-solving problems you already solved. Your AI gets sharper. And you end up with an actual archive of how the thing was built — not just what it became.

---

## Not the first to think this

chronicl.md didn't arrive from nowhere. It sits alongside a few related ideas already doing the rounds:

- **llms.txt** — a human-readable primer for AI on your repo
- **Telos** — structured narrative built for LLMs
- **claude.md** — Claude-flavoured project context
- **Cursor's rules** — persistent context baked into the workflow

The difference: chronicl.md isn't a spec. It's a practice you can start today, on any project, without adopting an ecosystem.

---

## The workflow

1. Start with the template. Fill in the basics.
2. Log as decisions happen. A bullet point takes ten seconds.
3. Journal regularly — one entry per branch or feature is a good rhythm.
4. Review before merging. Keep it current, not cluttered.
5. Adapt it. It's your file.

---

## Why bother

For humans: clarity, ownership, a shared source of truth.

For AI: memory that survives the session.

For the project: a record that actually means something six months from now.

---

## Try it

Start with three sections. Ten minutes, tops.

The value isn't in the setup. It's in the entries you keep adding.

→ [Read the docs](https://chronicl.dev)

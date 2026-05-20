---
title: The Dobby Club API
slug: the-dobby-club
type: project
date: 2024-01-01
tags: [api, python, fastapi, supabase, open-source, side-project]
project: the-dobby-club
---

# The Dobby Club API

## The Brief

There was no brief. No client, no deadline, no business case. Just a developer who wanted to learn FastAPI and Supabase, and a favourite TV show that happened to have an inexhaustible supply of quotable material.

Peep Show is a UK sitcom with a devoted following and a quote culture that borders on its own language. If you've watched it, you already know. The Dobby Club API is the inevitable result of someone who loves the show and needed a real project to learn on.

## The Problem

Not every project needs a problem statement. This one needed a dataset worth building around and endpoints worth caring about.

The Peep Show community is built on quotes. Lines get referenced in conversation, dropped into forums, shared as memes. But there was no structured, searchable resource for any of it — no way to query the full scripts, find where a line came from, or get a random quote at will. A small gap. Absolutely worth filling.

## The Approach

Pick something you love. Build something real. Learn by doing.

FastAPI and Supabase were the deliberate choices — both unfamiliar at the time, both things worth understanding properly. The project became the classroom. Rather than following tutorials in isolation, every concept got tested against an actual running API with real data, real endpoints, and the occasional Peep Show meme stored in a Supabase bucket.

The API was open source from the start, MIT licensed, with a contributing guide for anyone who wanted to add to it. That wasn't an afterthought — building in public and inviting contribution was part of the point.

## The Work

A RESTful API serving the complete Peep Show dataset — characters, actors, episodes, series, locations, scripts, quotes, audio clips, avatars, and memes. Ten endpoints, all publicly accessible for GET requests, with API key authentication gating any write operations.

The quotes endpoint is the centrepiece. Full script search across every series and episode — find any line, see exactly who said it, in which episode, in which series. Or go the other way: request a random quote and let the show surprise you.

The docs live at thedobby.club/docs — Swagger UI built into FastAPI, interactive and ready to use without any setup. The whole thing runs on Vercel, backed by Supabase, containerised with Docker.

76 commits. One fork. A Postman collection. A README with a meme. Everything a good side project should have.

## The Outcome

Still live. Still running. And quietly useful to people beyond its creator.

Members of the open source community picked it up and started using it as a teaching resource — a clean, well-documented example API for lectures and demonstrations. That wasn't planned. It's the best kind of outcome: something built for fun, finding a life of its own.

It's unfinished and proudly so. A first look at FastAPI and Supabase that became the foundation everything since was built on. The refactor will come eventually. The pride in shipping it is already here.

## Stack & Tools

- **Python** — primary language
- **FastAPI** — API framework
- **Supabase** — database and storage
- **Vercel** — deployment and hosting
- **Docker** — containerisation
- **Swagger UI** — built-in API documentation

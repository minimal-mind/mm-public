---
title: Mercury
slug: mercury
type: project
date: 2025-01-01
tags: [open-source, python, sdk, automation, broadworks, cli, async, telephony]
project: mercury
---

# Mercury

## The Brief

BroadWorks is one of the most widely deployed telephony platforms in the world. It is also, by most accounts, a nightmare to build on top of.

The platform has interfaces — OCIP being the primary one — but working with them directly means wrestling with raw XML schemas, manual connection orchestration, and a development experience that feels designed to discourage automation rather than enable it. Mercury was built to change that: a Python SDK that wraps the BroadWorks OCIP interface in a clean abstraction layer, making the platform programmable in the way it always should have been.

The result is not a single tool but an ecosystem — three components targeting three distinct personas, from the developer who wants raw async speed to the engineer who just wants to stop doing things manually.

## The Problem

Before Mercury, automating anything in BroadWorks was either painful, slow, or simply not done.

The OCIP interface exists, but working with it directly requires the correct schemas, careful connection handling, significant orchestration, and a tolerance for raw XML that most modern engineers don't have and shouldn't need. Anything in bulk had to be done manually — hours of repetitive configuration that couldn't be scripted. Orchestration around the platform was effectively impossible. Scheduled tasks, scaled configuration, conditional logic — none of it was accessible without significant bespoke engineering per use case.

Existing open-source solutions existed but were narrow — limited to either SOAP or TCP, limited in feature set, and not built with production engineering teams in mind. The gap was real, and the cost of it was measured in engineer-hours spent on work that should never have required a human.

## The Approach

The solution started as a single SDK and grew into a three-tier ecosystem shaped by a lesson learned early: handing an SDK to a non-developer and expecting them to run with it doesn't work. You end up trying to turn engineers into developers, and engineers don't want to learn to code — they want their problems solved.

That insight drove the architecture. Rather than a single monolithic tool, Mercury became a layered ecosystem built around personas:

- The **SDK** for developers who want to build with BroadWorks programmatically
- The **CLI** for engineers and administrators who want automation without writing code
- The **async engine** for developers building enterprise-scale applications on top of BroadWorks

Each layer uses the one beneath it. Each serves a distinct audience. Together they cover the full spectrum of who actually works with BroadWorks.

## The Work

### Mercury OCIP — The SDK

The core SDK, written in Python 3.12, managed with uv — Astral's modern Python package manager chosen for its speed, reliability, and the quality of the tooling around it. Published on PyPI as `mercury-ocip`.

The SDK supports both BroadWorks connection types — SOAP and TCP — simultaneously. Most comparable tools pick one. Mercury handles both, abstracting the connection layer entirely so the developer doesn't need to think about transport.

Under the hood, the BroadWorks XML schemas are run through a custom-built parser that generates Pydantic classes from the raw schema definitions. Pydantic was the deliberate choice here — the type safety, validation speed, and memory efficiency it provides at the client level is material when you're running bulk operations against a live telephony platform. The schema coverage is extensive: the full OCI-P command set, wrapped in Python objects with clean response types that serialise to dict, JSON, or XML.

On top of the raw command layer sits the Agent — a higher-order abstraction providing automation features that BroadWorks itself doesn't offer. Alias lookup, bulk user creation from CSV, automated configuration workflows. The things engineers were doing manually, now done in a single method call.

67 commits. 13 releases. MIT licensed.

### Mercury CLI — The Terminal Interface

When the SDK reached non-developer engineers, the feedback was consistent: they didn't want to write Python. They wanted the features.

The CLI is a terminal wrapper around Mercury OCIP, exposing the core automation and bulk operation features through a command-line interface that engineers can actually use. It doesn't attempt to replicate the full SDK surface — that's not the point. The point is that the automation features, the bulk upload sheets, the things people actually need to do repeatedly in BroadWorks — those are all accessible without writing a line of code.

It targets the engineer persona precisely: comfortable in a terminal, not interested in a Python REPL.

### Mercury OCIP Fast — The Async Engine

The third component is a stripped-down async version of the SDK, built for developers who need to build production applications on top of BroadWorks at scale.

Where Mercury OCIP is synchronous and feature-rich, OCIP Fast is asynchronous and deliberately lean. No automation helpers. No bulk operations. Just the full schema set wrapped in a lightweight async client that opens multiple connections to BroadWorks and load-balances across them per client instance. Designed from the ground up for speed and throughput — the kind of thing you put in the backend of a BroadWorks-facing application and trust to handle the volume.

It exists because there's a third persona the SDK and CLI don't serve: the developer who isn't

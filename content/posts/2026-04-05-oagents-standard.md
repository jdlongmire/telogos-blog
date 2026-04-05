---
title: "OAgents: An Open Standard for AI Agent Trust"
date: 2026-04-05
draft: false
categories: ["AI Standards"]
tags: ["oagents", "nist", "ai-rmf", "behavioral-envelope", "standards"]
summary: "We published an open standard for making AI agents operationally trustworthy. It maps to the NIST AI Risk Management Framework, has a Zenodo DOI, and includes a sanitized reference implementation. Here's what it is and why it matters."
author: "JD Longmire"
---

AI agents are getting deployed in operational roles — deploying code, managing infrastructure, generating documents, responding to incidents. The models are capable enough. The problem is trust.

When a human operator deploys code to production, you trust them because of training, code review, change management, and accountability. When an AI agent does the same thing, none of those mechanisms exist by default. No persistent memory of past mistakes. No independent reviewer. No process gate that can't be bypassed with a clever prompt. No institutional knowledge that survives the session.

That's the gap. Not capability — trust.

## What OAgents Is

OAgents is an open standard for behavioral envelopes — structured gates that wrap an AI agent to make its behavior reliable, auditable, and self-improving. The standard defines 26 components across 7 categories, organized into 3 compliance levels.

The standard is model-agnostic. The behavioral guarantees are properties of the envelope, not properties of the underlying model. Swap from GPT to Gemini to Claude to a local model — the trust layer stays the same.

## The OAuth Parallel

In the early 2000s, web applications needed to share user data across platforms. The only mechanism was sharing passwords. OAuth fixed that with a standardized trust layer: scoped tokens, verifiable by any party.

AI agents have the same structural problem. Organizations need to delegate operational authority to AI agents, but the only mechanism is prompt instructions — unverifiable, unenforceable, forgotten when context compresses.

OAgents is the trust layer for AI agent operations. Not a product. Infrastructure.

## What's In the Standard

Seven component categories:

1. **Behavioral Shaping** — persistent memory that survives across sessions, named failure mode catalogs the agent self-monitors for, context degradation detection
2. **Quality Gates** — independent output review by a separate model, executable process enforcement, security auditing, schema validation
3. **Operational Discipline** — mandatory session protocols, impact level classification, incident lifecycle tracking, structured logging
4. **Knowledge Injection** — persistent memory system, domain skill loading, lessons-learned pipeline that feeds failures back into prevention
5. **Enforcement Mechanisms** — executable gates (git hooks, CI checks) that can't be bypassed by prompt engineering, severity escalation, protocol compliance verification
6. **Project Governance** — centralized backlog, platform sovereignty, asset registry, vendor independence
7. **Anti-Hallucination** — state verification before assertions, memory staleness detection, hallucination tracking with recurrence analysis

Each component is classified as MUST (required for compliance) or SHOULD (recommended for production). Three compliance levels — Basic, Standard, Autonomous — support incremental adoption.

## NIST Alignment

The standard is presented as an Implementation Profile of the NIST AI Risk Management Framework (AI RMF 1.0). Every component maps to AI RMF functions: GOVERN, MAP, MEASURE, MANAGE. The full subcategory mapping is in the appendices.

This isn't just an academic alignment. Federal agencies operating under Executive Order 14110 need implementation frameworks for AI agent trustworthiness. OAgents provides that framework.

## The Reference Implementation

We didn't just write a spec. There's a sanitized reference implementation in the repository showing how all 26 components are implemented in a production environment managing 20+ enterprise services. Git hooks, session scripts, QA agents, memory schemas, ops log formats — all published, all inspectable.

The spec says "here's what you need." The reference shows "here's what it looks like."

## Where to Find It

- **Repository:** [github.com/ologos-corp/OAgents-standard](https://github.com/ologos-corp/OAgents-standard)
- **DOI:** [10.5281/zenodo.19425021](https://doi.org/10.5281/zenodo.19425021)
- **License:** CC BY 4.0 — use it, implement it, extend it

The taxonomy is open. No permission needed. If you implement the MUST-level components at the specified compliance level, you're conformant. That's how standards work.

## What This Isn't

This isn't a product announcement. There's nothing to buy. OAgents is a specification — the same kind of thing OAuth was before Google and Facebook built implementations of it. The standard is free. Implementations are the community's job.

The model is a commodity. Trust is the product.

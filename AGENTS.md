# AGENTS.md

This file provides repository-wide instructions for coding agents working in GovTestPrep.

## Mission

GovTestPrep is a platform-oriented monorepo intended to support multiple test prep websites on a shared product line. Agents should optimize for reusability, multi-tenant design, and clean separation between shared platform logic and site-specific content.

## Core Principles

1. Build shared infrastructure before site-specific duplication.
2. Keep tenant or site variation in config and content whenever possible.
3. Prefer simple scaffolds and explicit documentation over premature complexity.
4. Keep files easy for future human engineers and agents to extend.
5. Do not hardcode a single exam or brand into shared layers unless explicitly instructed.

## Architectural Guidance

- Shared product code belongs in `apps/` and `packages/`.
- Site-specific content belongs in `content/sites/<site-id>/`.
- Agent-specific workflows and prompts belong in `agents/`.
- New code should assume multiple websites may run on the same backend and frontend foundation.
- Favor content-driven and config-driven approaches over branching the application per site.

## When Adding Features

Agents should ask:
- Is this shared platform logic or site-specific content?
- Can this be modeled through config instead of custom code?
- Will this make launching the next site easier?
- Does this preserve a clean separation between content, presentation, and business logic?

## Content and Exam Model

Assume the platform will eventually support:
- multiple exam categories
- lessons and study guides
- question banks and explanations
- user progress and performance data
- paid and free product tiers

Design new assets with these future requirements in mind.

## Implementation Preference

When the user asks for scaffolding or early setup:
- create small, clear files
- document intent in READMEs
- avoid overcommitting to frameworks too early unless asked
- keep conventions easy to automate later

## Do Not

- Do not collapse all site content into shared app directories.
- Do not assume there will only ever be one site.
- Do not introduce unnecessary complexity for speculative edge cases.
- Do not overwrite user-authored strategic documentation without preserving intent.

## Delivery Style

When updating this repo, prefer changes that improve:
- platform reuse
- future site launch speed
- clarity for application engineers
- clarity for future agents

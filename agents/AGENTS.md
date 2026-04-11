# AGENTS (Agents Directory)

This directory contains agent workspaces.

## Purpose

Agents are responsible for generating, transforming, and maintaining structured content and supporting assets.

## Expected Agent Types

- content generation agents (questions, lessons)
- QA and validation agents
- SEO and landing page generation agents
- curriculum planning agents

## Output Expectations

Agents should primarily output structured data into `content/`.

## Rules

- Do not write directly into shared app logic unless explicitly required.
- Prefer generating content and structured assets over modifying platform code.
- Ensure outputs are deterministic and reusable when possible.

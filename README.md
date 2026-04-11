# GovTestPrep

GovTestPrep is a platform-oriented monorepo for launching multiple federal and government-adjacent online test prep websites from a shared product foundation.

---

## Purpose

The goal is to support a family of exam-prep properties that share:

- a common frontend shell  
- a common backend and data model  
- shared UI and business logic  
- agent-assisted content production  
- site-specific content and branding  

This repo is structured so future application engineering can launch new websites primarily by adding content and configuration—not rebuilding infrastructure.

---

## Platform Model

The architecture is **multi-tenant by design**.

A single platform can power multiple sites such as:

- USPS exam prep  
- FAA / Air Traffic Controller exam prep  
- federal hiring assessments  
- contractor certification prep  
- other government-adjacent certification products  

Each site varies by:

- branding  
- exam type  
- SEO content  
- question banks  
- lessons and curriculum  
- pricing  

While reusing the same core application.

---

## Repository Structure

apps/
web/ Shared frontend shell
api/ Shared backend services

packages/
ui/ Shared reusable UI components

content/
sites/
example-site/ Example site config + content

agents/
content-agent/ Agent workspace for content generation


---

## Directory Intent

### apps/web
Shared frontend application.  
Future: multi-tenant routing, theming, reusable page templates.

### apps/api
Shared backend.  
Future: auth, payments, user progress, question delivery, multi-tenant data model.

### packages/ui
Shared component library across all sites.

### content/sites
Where **all site-specific differentiation lives**:
- config
- lessons
- questions
- landing pages
- SEO content

### agents
Where your **AI workforce** lives:
- content generation
- QA/validation
- SEO page generation
- curriculum planning

---

## How to Add a New Site

The intended pattern:

1. Create a folder:content/sites/<site-id>/
  
2. Add:
- config.json
- content (questions, lessons, pages)

3. Hook into frontend routing

4. Deploy

👉 No duplication of apps or backend required

---

## Current State

This repo is an early scaffold designed to support:

- platform-first architecture
- agent-driven content creation
- scalable multi-site expansion

---

## Near-Term Priorities

1. Define content schema (questions, lessons, exams)
2. Define site configuration format
3. Build frontend shell (multi-tenant)
4. Build backend (tenant-aware)
5. Build agent pipelines for content generation

---

## Guiding Principle

**Build once at the platform level.  
Differentiate at the content level.**

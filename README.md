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

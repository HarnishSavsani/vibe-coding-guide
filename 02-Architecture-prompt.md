# Role
You are a principal Software Architect with deep experience designing modern full-stack applications (web, mobile, and APIs). You create architecture documentation that is both human-readable and highly usable by AI coding agents. You favor pragmatic, proven patterns over academic or over-engineered solutions.

Your diagrams are always valid Mermaid syntax and easy to understand at a glance.

# Context
I already have (or will create) a PRD.md for this project. Now I need a comprehensive `Architecture.md` that describes how the system will be built. This document will guide all subsequent coding, folder structure decisions, and AI generation.

# Project Information (FILL THESE IN)
- **Project Name**: [PROJECT_NAME]
- **Short summary of what the product does**: [2–4 sentences]
- **Key features from PRD** (list the most important ones): 
  - ...
  - ...
- **Preferred / already decided tech stack** (if any): [e.g. Next.js 15 App Router, TypeScript, Tailwind CSS, Supabase, Vercel]
- **Deployment target**: [Vercel / Railway / AWS / Fly.io / Self-hosted / Mobile stores / etc.]
- **Special requirements**: [real-time, offline-first, multi-tenant, high concurrency, strict compliance, etc.]
- **Team / solo context**: [solo developer, small team, etc.]
- **Any strong architectural preferences or constraints**: [e.g. prefer serverless, must use PostgreSQL, avoid GraphQL, etc.]

# Task
Generate a complete, high-quality `Architecture.md` file that an AI agent can use as the structural blueprint of the entire project.

# Required Output Structure (follow exactly)

```markdown
# [PROJECT_NAME] – System Architecture

**Last Updated**: [YYYY-MM-DD]  
**Status**: Draft  
**Related Documents**: PRD.md, Specs.md, Rules.md

---

## 1. Architectural Goals & Principles
List 5–7 guiding principles for this architecture (e.g. simplicity first, type safety, clear boundaries, observability, etc.).

## 2. High-Level System Overview
Write 2–4 paragraphs describing the overall shape of the system, major components, and how they interact. Mention the primary architectural style (monolith, modular monolith, microservices, serverless, Jamstack, etc.) and why it was chosen.

## 3. System Context Diagram (C4 Level 1)
```mermaid
C4Context
title System Context - [PROJECT_NAME]
... (complete valid Mermaid C4Context or a clean flowchart if C4 is overkill)

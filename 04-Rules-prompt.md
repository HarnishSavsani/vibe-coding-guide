# Role
You are a principal Engineer and Engineering Manager who writes clear, enforceable coding standards and AI guardrails. Your Rules.md files are designed to keep AI coding agents (and human developers) consistent, safe, and productive. You prevent common AI failure modes: hallucinated libraries, over-engineering, inconsistent patterns, and security mistakes.

# Context
I need a strong `Rules.md` (can also be used as `.cursorrules`, `CLAUDE.md`, or `AGENTS.md`) that will be included in every AI coding session for this project. This file is the permanent constitution of the codebase.

# Project Information (FILL THESE IN)
- **Project Name**: [PROJECT_NAME]
- **Primary Tech Stack**: [list exact technologies – e.g. Next.js 15, React 19, TypeScript 5.x, Tailwind CSS 4, Supabase, Zod, etc.]
- **Key principles I care about most**: [e.g. type safety, simplicity, performance, accessibility, testability, minimal dependencies]
- **Things I strongly want to avoid**: [e.g. unnecessary abstraction, certain libraries, class-based components, any types, etc.]
- **Codebase size / team context**: [solo, small team, greenfield, existing large codebase]
- **Any existing style decisions already made**: [list them]

# Task
Generate a comprehensive, actionable `Rules.md` file that an AI agent must follow on every coding task.

# Required Output Structure (follow exactly)

```markdown
# [PROJECT_NAME] – Coding Rules & AI Guardrails

**Last Updated**: [YYYY-MM-DD]  
**Status**: Active – must be followed by all AI agents and contributors

> **Instruction to AI**: Read this entire file before writing or modifying any code. These rules override your default preferences.

---

## 1. Core Philosophy
List 5–8 short, memorable principles that guide every decision in this project.
Example style:
- Simplicity over cleverness
- Explicit over implicit
- Type safety is non-negotiable
- …

## 2. Technology & Dependency Rules

### 2.1 Approved Stack (do not deviate without discussion)
| Category          | Approved Choice              | Notes |
|-------------------|------------------------------|-------|
| ...               | ...                          | ...   |

### 2.2 Libraries – Allowed
List libraries that are pre-approved and preferred.

### 2.3 Libraries – Forbidden or Strongly Discouraged
Be explicit. Examples of common AI mistakes to block:
- Do not install new UI libraries without approval
- Do not use moment.js / lodash full / jQuery
- Do not add state management libraries if the stack already has a solution
- etc.

### 2.4 When you need a new dependency
Describe the exact process the AI must follow (e.g. “Propose it first and wait for confirmation”, “Add to package.json only after explicit approval”).

## 3. Code Style & Organization

### 3.1 Naming Conventions
- Files
- Components
- Functions
- Variables
- Types / Interfaces
- Constants
- CSS classes / Tailwind

### 3.2 File & Folder Rules
- Where new files should be created
- Maximum file length guidelines
- When to split files
- Index files / barrel exports policy

### 3.3 TypeScript / Language Rules
- Strictness level
- Use of `any` / `unknown`
- Preference for interfaces vs types
- Enum vs union types
- Zod or other validation usage

### 3.4 React / Frontend Specific Rules (if applicable)
- Server vs Client Components
- Hooks rules
- State management approach
- Component composition patterns
- Prefer function components only, etc.

### 3.5 Backend / API Rules (if applicable)
- Route handler patterns
- Validation
- Error response shape
- Database access patterns

## 4. Error Handling & Resilience
- How errors should be caught and propagated
- User-facing error messages vs internal logs
- Retry strategies
- Fallback UI
- Never swallow errors silently

## 5. Security Rules
- Secrets management
- Input validation (always)
- Authentication & authorization checks
- SQL / NoSQL injection prevention
- XSS prevention
- CSRF
- Rate limiting expectations
- What must never be logged

## 6. Testing Expectations
- What must have tests
- Preferred testing tools and patterns
- What is acceptable to leave untested in early phases
- Snapshot testing policy

## 7. Performance & Accessibility
- Bundle size awareness
- Image optimization rules
- Core Web Vitals targets (if web)
- Accessibility checklist the AI must follow (focus states, labels, contrast, keyboard navigation)

## 8. AI-Specific Guardrails (Critical Section)

### Always do
- …
- Read Memory.md and Rules.md before starting work
- Prefer editing existing files over creating new ones when possible
- …

### Never do
- Never invent APIs or database columns that are not in Specs.md / Architecture.md
- Never install packages without explicit instruction
- Never commit secrets or .env files
- Never use `@ts-ignore` or `any` to silence errors
- Never create giant god components or files
- …

### When uncertain
- Ask a clarifying question
- Or create a clearly marked TODO and update Memory.md
- Or propose 2–3 options and wait

## 9. Documentation & Comments
- When to write JSDoc / TSDoc
- Inline comment policy
- README and docs update expectations

## 10. Git & Commit Expectations (if relevant)
- Commit message style
- What not to commit

## 11. How to Update This Rules File
Describe the process so the AI knows when and how to propose changes to Rules.md itself.

---

# Quality Criteria
- Rules must be actionable (“Do X”, “Never do Y”)
- AI-specific section must be extremely clear
- No conflicting rules
- Prefer short, scannable bullets and tables
- The file should be readable in under 5–7 minutes

# Output Instructions
1. Output only the final Markdown of Rules.md.
2. Start with:
   `<!-- PERMANENT RULES – AI agents must read this before every coding session -->`
3. Make the “AI-Specific Guardrails” section especially strong and explicit.
4. Use bold or callouts for the most critical never-do rules.

# Role
You are a senior Technical Product Manager and Spec Writer who creates precise, unambiguous, implementation-ready specifications. Your specs are written so that both human developers and AI coding agents can implement features correctly on the first attempt with minimal clarification.

You hate ambiguity. You turn vague ideas into concrete, testable contracts.

# Context
I have a PRD.md and Architecture.md (or will provide summaries). Now I need a detailed `Specs.md` that expands every important feature into clear, implementable specifications. This document is the detailed contract for “what exactly should be built”.

# Project Information (FILL THESE IN)
- **Project Name**: [PROJECT_NAME]
- **Link or summary of PRD**: [paste key sections or short summary]
- **Link or summary of Architecture**: [especially data model, major modules, tech stack]
- **Scope of this Specs document**: [Entire MVP / Specific epic / Full product]
- **Any already decided detailed behaviors**: [list them]

# Task
Generate a complete, high-quality `Specs.md` file that can be used directly by AI coding tools as the source of truth for feature implementation.

# Required Output Structure (follow exactly)

```markdown
# [PROJECT_NAME] – Detailed Product Specifications

**Last Updated**: [YYYY-MM-DD]  
**Version**: 0.1  
**Status**: Draft  
**Related Documents**: PRD.md, Architecture.md, Rules.md

---

## 1. Introduction & Scope
- What this document covers
- What is explicitly out of scope for this version
- How this document relates to the PRD and Architecture

## 2. Definitions, Glossary & Conventions
| Term / Abbreviation | Definition |
|---------------------|------------|
| ...                 | ...        |

Also define any naming conventions used in the specs (e.g. how IDs look, status values, etc.).

## 3. Global Rules & Shared Behaviors
Document rules that apply across multiple features:
- Authentication & session behavior
- Authorization / permission model
- Validation philosophy
- Error response format (for APIs)
- Pagination, filtering, sorting conventions
- Soft delete vs hard delete
- Timestamps and timezone handling
- Audit logging (if any)

## 4. Feature Specifications
Organize by major feature or domain. Use a consistent template for every feature:

### 4.1 [Feature Name] (e.g. User Authentication)
**Priority**: P0 / P1 / P2  
**PRD Reference**: US-00X, FR-00Y  
**Owner Module / Area**: [from Architecture]

#### 4.1.1 Description
Clear description of what this feature does and why it exists.

#### 4.1.2 User Flows
Describe the main happy path and important alternative paths in numbered steps or with a small Mermaid flowchart/sequence if helpful.

#### 4.1.3 Detailed Functional Behavior
Break down into precise rules:
- What the system does in each situation
- Business rules
- Calculations or derived data
- State transitions (prefer a small state diagram if complex)

#### 4.1.4 Data & API Contracts
- Database fields involved (name, type, constraints, defaults)
- API endpoints (method, path, request body, response body, status codes)
- Events emitted or consumed (if event-driven)

Use tables or TypeScript-like interfaces for clarity.

#### 4.1.5 Acceptance Criteria
Use Given / When / Then format. Cover:
- Happy path
- Important alternative paths
- Authorization cases
- Validation failures

#### 4.1.6 Edge Cases & Error Handling
List specific edge cases and the exact expected behavior (including error messages where user-facing).

#### 4.1.7 UI / UX Requirements (if applicable)
- Key screens or components involved
- Empty states
- Loading states
- Error states
- Accessibility notes specific to this feature

#### 4.1.8 Non-Functional Notes for this Feature
Any performance, security, or scalability requirements specific to this feature.

---

(Repeat the entire 4.x template for every major feature)

Recommended major feature sections for most products:
- Authentication & Account Management
- Core Domain Feature(s)
- Settings / Profile
- Notifications (if any)
- Admin / Internal tools (if any)
- Billing / Payments (if any)

## 5. Data Model Details
Expand the high-level data model from Architecture.md:
- Full field lists with types and constraints
- Relationships and cardinality
- Important indexes
- Cascading rules
- Any denormalization decisions

Prefer tables + optional Mermaid erDiagram.

## 6. Cross-Cutting Technical Specifications
- API design conventions (REST / tRPC / GraphQL style)
- Authentication token handling
- File upload specifications (if any)
- Background job specifications (if any)
- Email / notification templates and triggers

## 7. Out of Scope (Reinforced)
Explicit list of things that must not be implemented in the current version, even if they seem related.

## 8. Open Specifications & TBD Items
Numbered list of items that still require product or technical decisions.

---

# Quality Criteria (must all be true)
- Every P0 feature has clear Acceptance Criteria in Given/When/Then form
- No ambiguous language (“should be fast”, “handle errors gracefully”)
- Data contracts are specific enough to implement without guessing field names or types
- Edge cases are explicitly addressed
- An AI agent reading only this document + Architecture.md should be able to implement the feature correctly

# Output Instructions
1. Output only the final Markdown content of Specs.md.
2. Start with:
   `<!-- Generated with detailed vibe-coding Specs prompt. Keep in sync with PRD and Architecture. -->`
3. Use consistent numbering (Feature 4.1, 4.2…).
4. Prefer tables and structured lists over long paragraphs.
5. If a section is not applicable, write “N/A – [reason]” instead of omitting it.

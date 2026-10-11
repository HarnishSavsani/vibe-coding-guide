# Role
You are a senior Product Manager and technical founder with 12+ years of experience writing Product Requirements Documents for startups and scale-ups. You specialize in creating concise yet comprehensive PRDs that serve as the single source of truth for both human developers and AI coding agents (Cursor, Claude Code, Windsurf, etc.).

Your writing style is:
- Clear and unambiguous
- Testable (every requirement can be verified)
- Developer-friendly
- Free of vague language (“easy”, “fast”, “user-friendly”, “intuitive”, “robust”)
- Structured with Markdown best practices

# Context
I am starting a new software project and need a high-quality `PRD.md` file. This document will be the foundation for Architecture, Specs, Rules, Phases, and all future AI coding sessions. It must be detailed enough that an AI agent can understand exactly what to build without constant clarification.

# Project Information (FILL THESE IN BEFORE RUNNING THE PROMPT)
- **Project Name**: [PROJECT_NAME]
- **One-line description**: [ONE_LINE_DESCRIPTION]
- **Target platform(s)**: [Web / Mobile (iOS+Android) / Desktop / API-only / Multi-platform]
- **Primary tech preference** (optional): [e.g. Next.js 15 + TypeScript + Tailwind + Supabase]
- **Business / personal goal**: [Why are we building this? What problem does it solve in the real world?]
- **Current stage**: [Pure idea / Validated idea / MVP / V1 / Internal tool]
- **Target launch timeline** (optional): [e.g. 6 weeks, weekend project, no hard deadline]
- **Any existing constraints or decisions already made**: [list them here]

# Task
Generate a complete, production-ready `PRD.md` file following the exact structure below. Do not skip any section. If information is missing, make reasonable, clearly marked assumptions and list them in the Assumptions section.

# Required Output Structure (follow this hierarchy exactly)

```markdown
# [PROJECT_NAME] – Product Requirements Document

**Status**: Draft  
**Last Updated**: [Today’s date in YYYY-MM-DD]  
**Owner**: [Your name or "Project Owner"]  
**Version**: 0.1

---

## 1. Overview
Write 3–5 clear sentences that answer:
- What are we building?
- Who is it for?
- Why does it matter right now?
- What is the core value proposition in one sentence?

## 2. Problem Statement
Describe the problem in concrete terms.
- What pain exists today?
- Who feels this pain?
- How are people currently solving (or failing to solve) it?
- What is the cost of the problem (time, money, frustration)?
If you have any data, anecdotes, or observations, include them. If not, state that this is based on assumption.

## 3. Target Users & Personas
### Primary Persona
- Name (fictional)
- Demographics / role
- Goals
- Frustrations
- Tech savviness
- Jobs-to-be-Done (JTBD format: “When I…, I want to…, so I can…”)

### Secondary Persona (if relevant)
Same structure as above.

### Anti-Persona (who this is NOT for)
Briefly describe who we are intentionally not serving.

## 4. Goals & Success Metrics
### Primary Goals
List 3–5 high-level goals for this version of the product.

### Success Metrics (must be measurable)
| Metric                        | Target          | Measurement Method       | Timeframe      |
|-------------------------------|-----------------|--------------------------|----------------|
| e.g. Weekly Active Users      | 500             | Analytics                | 90 days post-launch |
| e.g. Task completion rate     | ≥ 85%           | In-app tracking          | First 30 days  |
| ...                           | ...             | ...                      | ...            |

### Guardrail Metrics (things that must not get worse)
List any metrics that should not regress.

### Non-Goals (explicitly out of scope for this version)
This section is critical. List features or ambitions we are deliberately not doing now.

## 5. User Stories / Core Use Cases
Organize by priority:

### P0 – Must Have (MVP)
For each story use this exact format:

**US-001**: As a [persona], I want [action] so that [benefit].

**Acceptance Criteria**:
- Given [precondition]
- When [action]
- Then [expected result]
- And [additional expected result if needed]

### P1 – Should Have
Same format.

### P2 – Could Have / Nice to Have
Same format (can be shorter).

Aim for 8–15 well-written user stories total for a typical MVP.

## 6. Functional Requirements
Number them clearly (FR-001, FR-002…).

Each requirement must be:
- Atomic (one thing)
- Testable
- Written in the form: “The system shall…” or “The user shall be able to…”

Group related requirements under sub-headings if helpful (e.g. Authentication, Core Workflow, Notifications).

## 7. Non-Functional Requirements
Cover at minimum:

- **Performance**: response times, load targets
- **Security & Privacy**: authentication method, data protection, compliance (GDPR, etc. if relevant)
- **Accessibility**: WCAG level target
- **Reliability / Availability**: uptime expectations
- **Scalability**: expected concurrent users or data volume
- **Usability**: any specific constraints
- **Compatibility**: browsers, devices, OS versions

Be as concrete as possible (e.g. “Page load < 2s on 4G” instead of “fast”).

## 8. Constraints & Assumptions
### Constraints
- Technical
- Business / budget / time
- Legal / regulatory
- Third-party dependencies

### Assumptions
List every important assumption you made while writing this PRD. Mark them clearly so they can be validated later.

## 9. Open Questions & Decisions Needed
Numbered list of unresolved items that must be answered before or during development.

## 10. Appendix (optional but recommended)
- Glossary of domain terms
- Competitive landscape (brief)
- Inspiration / reference products
- Links to any existing research or notes

---

# Quality Criteria (you must satisfy all of these)
- No vague adjectives without measurable criteria
- Every P0 user story has clear Given/When/Then acceptance criteria
- Non-Goals section is present and meaningful
- Success metrics are specific and measurable
- The document can be understood by an AI agent that has never seen the project before
- Total length should typically be 400–800 lines (detailed but not bloated)

# Output Instructions
1. Output only the final Markdown content of PRD.md (no extra commentary before or after).
2. Start the file with this HTML comment:
   `<!-- Generated with detailed vibe-coding PRD prompt. Review assumptions and open questions carefully. -->`
3. Use proper Markdown (headings, tables, lists, bold for emphasis).
4. If any section cannot be fully filled due to missing information, write a clear placeholder and move the uncertainty to “Open Questions” or “Assumptions”.

# Role
You are an experienced Technical Lead and Delivery Manager who has shipped dozens of products. You excel at breaking work into logical, low-risk, incremental phases that deliver value early and reduce uncertainty. You optimize for learning, feedback, and continuous progress rather than big-bang releases.

# Context
I have PRD.md, Architecture.md, and Specs.md (or summaries of them). I now need a practical `Phases.md` that turns the full product vision into a sequenced implementation plan.

# Project Information (FILL THESE IN)
- **Project Name**: [PROJECT_NAME]
- **Overall goal of this plan**: [Ship a usable MVP / Build full V1 / Internal tool ready for team / etc.]
- **Time or effort constraint** (optional): [e.g. 4 weeks solo, 2 months part-time, no hard deadline]
- **Team context**: [solo developer / pair / small team]
- **Biggest risks I want to de-risk early**: [list technical or product risks]
- **Any hard deadlines or external dependencies**: [list]
- **Preferred phase granularity**: [short phases of 3–7 days / larger phases of 1–2 weeks]

# Task
Generate a realistic, actionable `Phases.md` that an AI coding agent and I can follow step by step.

# Required Output Structure (follow exactly)

```markdown
# [PROJECT_NAME] – Implementation Phases

**Last Updated**: [YYYY-MM-DD]  
**Status**: Active Plan  
**Related Documents**: PRD.md, Architecture.md, Specs.md, Memory.md

---

## 1. Phasing Strategy
Explain in 1–2 paragraphs the overall approach:
- Why these phases were chosen
- Whether phases are vertical slices (user value) or layered
- How risk is being reduced early
- How progress will be measured

## 2. Phase Overview Table
| Phase | Name                    | Goal                              | Estimated Effort | Key Deliverable          | Exit Criteria (summary) |
|-------|-------------------------|-----------------------------------|------------------|--------------------------|-------------------------|
| 0     | Foundation              | ...                               | ...              | ...                      | ...                     |
| 1     | ...                     | ...                               | ...              | ...                      | ...                     |
| 2     | ...                     | ...                               | ...              | ...                      | ...                     |
| …     | …                       | …                                 | …                | …                        | …                       |

## 3. Detailed Phase Breakdown

### Phase 0 – Foundation & Project Setup
**Goal**:  
**Estimated Effort**:  
**Dependencies**: None (starting point)

**Scope – What will be done**:
- Repository setup
- Tooling (linting, formatting, TypeScript config, etc.)
- Core folder structure according to Architecture.md
- CI skeleton
- Environment variable handling
- Basic design tokens / theme if Design.md exists
- …

**Explicitly Out of Scope for this phase**:
- …

**Deliverables / Checklist**:
- [ ] …
- [ ] …
- [ ] …

**Exit Criteria (Definition of Done)**:
- All checklist items completed
- Project runs locally with no errors
- Memory.md initialized
- …

**Risks & Mitigations specific to this phase**:
- …

---

### Phase 1 – [Name]
**Goal**:  
**Estimated Effort**:  
**Dependencies**: Phase 0 complete

**Scope – Features & technical work** (reference Specs.md IDs where possible):
- …

**User-visible value at the end of this phase**:
- …

**Deliverables / Checklist**:
- [ ] …
- [ ] …

**Exit Criteria**:
- …
- Manual or automated verification steps

**Testing expectations for this phase**:
- …

**Documentation / Memory updates required**:
- Update Memory.md
- Update any relevant specs if discoveries were made

**Risks & Mitigations**:
- …

---

(Repeat the same detailed structure for Phase 2, Phase 3, …)

## 4. Future / Later Phases (Backlog)
List features or technical work that is intentionally deferred beyond the current plan, with rough priority.

## 5. Cross-Phase Practices
- How and when to update Memory.md
- Branching / PR strategy (if relevant)
- When to refactor vs when to keep moving
- Definition of “phase complete”
- How to handle scope changes mid-phase

## 6. Progress Tracking Advice
Suggest a simple way to track progress (e.g. checkboxes in this file + Memory.md Current Focus section).

---

# Quality Criteria
- Each phase should be completable and demonstrable on its own
- Early phases should reduce the highest risks
- Checklists must be concrete and actionable
- Exit criteria must be binary (done or not done)
- Estimates can be rough but should feel realistic for the stated constraints
- Prefer 4–7 phases for most projects (not too many, not too few)

# Output Instructions
1. Output only the final Markdown of Phases.md.
2. Start with:
   `<!-- Living implementation plan. Update status and checkboxes as work progresses. -->`
3. Use consistent phase numbering.
4. Make checklists copy-paste friendly for Memory.md.

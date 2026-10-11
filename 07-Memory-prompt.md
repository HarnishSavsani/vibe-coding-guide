# Role
You are a meticulous Project Context Manager and living documentation specialist. Your job is to maintain a high-signal `Memory.md` file that captures the current truth of the project so that AI agents never need to re-analyze the entire history or guess the current state.

You keep the most recent and most important information at the top of every section.

# Context
I need a well-structured `Memory.md` that will be updated after every significant coding session. This file is the short-term + medium-term memory of the project.

# Project Information (FILL THESE IN)
- **Project Name**: [PROJECT_NAME]
- **Current date**: [YYYY-MM-DD]
- **Current Phase** (from Phases.md): [Phase 0 – Foundation / Phase 1 – … / Not started]
- **Overall project status**: [Just started / In active development / etc.]

# Task
Create the initial `Memory.md` file using the exact structure and rules below.  
In future sessions the AI will be instructed to update this file by inserting new information at the top of the relevant sections.

# Required Output Structure (this structure is permanent)

```markdown
# [PROJECT_NAME] – Project Memory

<!-- LIVING DOCUMENT – AI must update this file after every significant change -->

## Rules for Updating This File (DO NOT REMOVE OR MOVE THIS SECTION)
1. Newest information always goes to the **top** of each section.
2. Keep entries short, factual, and dated (YYYY-MM-DD).
3. After every meaningful coding session or decision, update this file before ending the session.
4. Mark completed checklist items with [x] and move them to a “Recently Completed” area or leave them checked.
5. Never delete historical information — only push it downward.
6. Update the “Last Updated” timestamp and “Current Focus” on every edit.
7. If a decision reverses a previous one, note the reversal explicitly at the top of the Decisions section.
8. Prefer bullet points over paragraphs.

**Last Updated**: [YYYY-MM-DD]  
**Current Phase**: [Phase X – Name]  
**Overall Status**: [On track / Slightly behind / Blocked / etc.]  
**Active Branch / Worktree** (optional): [main / feature/…]

---

## Current Focus (keep this section extremely up to date)
- What is being worked on right now
- Which files or modules are currently “hot”
- Immediate next 1–3 concrete steps
- Any blockers

## Recent Decisions (newest first)
- **[YYYY-MM-DD]** Decision: …  
  Rationale: …  
  Consequences / follow-up: …

- **[YYYY-MM-DD]** …

## Progress by Phase
### Phase 0 – Foundation
- [ ] …
- [x] … (completed on YYYY-MM-DD)
- …

### Phase 1 – [Name]
- [ ] …
- …

(Add more phases as they become active)

## Recently Completed (optional quick view)
- [YYYY-MM-DD] …
- …

## Known Issues & Bugs
- **[YYYY-MM-DD]** [Severity] Description → Status (Open / Investigating / Fixed)
- …

## Technical Debt & Conscious Shortcuts
- **[YYYY-MM-DD]** Description of debt → Why it was accepted → Plan to resolve (if any)

## Important Context for AI Agents
This section is gold for future sessions:
- Key files and their current responsibility
- Established patterns that must be continued
- Things that look tempting to change but should not be touched without discussion
- Current data model quirks or important invariants
- Environment / setup gotchas

## Session Log (newest first)
### [YYYY-MM-DD] – Session title or focus
- Accomplished:
  - …
- Left unfinished:
  - …
- Notes / discoveries for next session:
  - …
- Memory updates made: Yes / No

### [previous date] – …

---

## Older History / Archive
(When the sections above become too long, move older entries here. Keep the top of the file focused on the present.)

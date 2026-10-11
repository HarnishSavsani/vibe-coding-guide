# Vibe Coding Foundation Docs – Detailed Prompt Pack

A complete set of **highly detailed, production-grade prompts** to generate the 7 essential Markdown documents that make AI-assisted (“vibe”) coding reliable, structured, and scalable.

These prompts are significantly expanded with:
- Strong role definition
- Explicit project placeholders
- Strict required output structure
- Quality criteria the AI must satisfy
- Clear output instructions
- Customization guidance
- Usage tips

## The 7 Documents

| # | File | Purpose |
|---|------|---------|
| 1 | **PRD.md** | What to build, target users, goals, user stories, functional & non-functional requirements |
| 2 | **Architecture.md** | System design, Mermaid diagrams (C4 + flows), folder structure, tech stack, ADRs |
| 3 | **Specs.md** | Detailed, testable feature specifications with Given/When/Then acceptance criteria |
| 4 | **Rules.md** | AI guardrails, approved/forbidden libraries, coding standards, security & error handling |
| 5 | **Phases.md** | Incremental delivery plan with checklists and exit criteria |
| 6 | **Design.md** | Complete design system (colors, typography, spacing, components, accessibility) |
| 7 | **Memory.md** | Living project memory – newest information always on top |

## Recommended Generation Order

```
1. PRD.md
2. Architecture.md
3. Specs.md
4. Rules.md
5. Phases.md
6. Design.md
7. Memory.md   ← start light, then keep updating after every session
```

## How to Use Each Prompt

1. Open the corresponding `0X-*-prompt.md` file.
2. Copy the entire content inside the big code block.
3. Fill in every `[PLACEHOLDER]` with your project details.
4. Paste the completed prompt into Cursor / Claude / ChatGPT / Windsurf / etc.
5. Save the AI’s output as the corresponding `.md` file in your project root (or `/docs`).

## Keeping Memory.md Alive

After every significant coding session, use the short update prompt provided at the bottom of `07-Memory-prompt.md`.

## Customization

Every prompt contains clear places where you can adapt the structure for your specific project (small MVP vs large product, web vs mobile, etc.). The core philosophy stays the same so all documents remain consistent with each other.

---

**Created for reliable vibe coding.**  
Fill the placeholders carefully — the quality of the generated documents is directly proportional to the quality of the information you provide.

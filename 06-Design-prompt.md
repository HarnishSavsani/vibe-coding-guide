# Role
You are a senior Product Designer and Design Systems lead who creates practical, developer-friendly design systems. You produce clear design tokens, typography scales, component guidelines, and accessibility rules that both designers and AI coding agents can implement consistently.

You balance aesthetics with implementability. You never leave values vague.

# Context
I need a complete `Design.md` that will serve as the visual and interaction source of truth for the project. AI agents will read this file when creating or modifying any UI.

# Project Information (FILL THESE IN)
- **Project Name**: [PROJECT_NAME]
- **Product feeling / brand personality**: [e.g. calm & trustworthy, bold & energetic, minimal & premium, playful & friendly, clinical & precise]
- **Primary platform(s)**: [Web responsive / Mobile app / Desktop / All]
- **Already decided brand elements** (if any):
  - Primary color(s): [hex or description]
  - Fonts: [names or “system fonts”]
  - Logo / existing assets: [describe or “none”]
- **Accessibility target**: [WCAG 2.1 AA / AAA / not specified]
- **Dark mode**: [Required / Nice to have / Not needed]
- **Inspiration references** (optional): [list 2–4 products or sites whose visual language you like]
- **Tech stack for styling**: [Tailwind CSS / CSS Modules / styled-components / vanilla CSS / etc.]

# Task
Generate a complete, implementation-ready `Design.md` file.

# Required Output Structure (follow exactly)

```markdown
# [PROJECT_NAME] – Design System

**Last Updated**: [YYYY-MM-DD]  
**Status**: Active  
**Related Documents**: Architecture.md, Rules.md

---

## 1. Design Principles
List 5–7 short principles that should guide every visual and interaction decision.
Examples of good principles:
- Clarity over decoration
- Consistency creates trust
- Generous whitespace
- …

## 2. Color System

### 2.1 Brand / Primary Colors
| Token Name       | Light Mode Hex | Dark Mode Hex | Usage                          |
|------------------|----------------|---------------|--------------------------------|
| primary-500      | #3B82F6        | #60A5FA       | Main actions, links            |
| primary-600      | ...            | ...           | Hover / active                 |
| …                | …              | …             | …                              |

### 2.2 Neutral / Gray Scale
Provide a full scale (50–950 or 10–12 steps).

### 2.3 Semantic Colors
| Token          | Light   | Dark    | Usage                    |
|----------------|---------|---------|--------------------------|
| success        | …       | …       | …                        |
| warning        | …       | …       | …                        |
| error          | …       | …       | …                        |
| info           | …       | …       | …                        |

### 2.4 Background & Surface Colors
Define background, card, elevated surface, overlay, etc.

### 2.5 Color Usage Rules
- When to use primary vs neutral
- Contrast requirements
- Do not use pure black or pure white if that is a principle

## 3. Typography

### 3.1 Font Families
- **Display / Headings**: [font name or stack]
- **Body**: [font name or stack]
- **Monospace**: [font name or stack]
- Fallback strategy

### 3.2 Type Scale
| Token     | Size (rem/px) | Weight | Line Height | Letter Spacing | Usage                  |
|-----------|---------------|--------|-------------|----------------|------------------------|
| display   | 3rem / 48px   | 700    | 1.1         | -0.02em        | Hero headings          |
| h1        | …             | …      | …           | …              | …                      |
| h2        | …             | …      | …           | …              | …                      |
| h3        | …             | …      | …           | …              | …                      |
| body-lg   | …             | …      | …           | …              | …                      |
| body      | …             | …      | …           | …              | Default body text      |
| body-sm   | …             | …      | …           | …              | …                      |
| caption   | …             | …      | …           | …              | …                      |

### 3.3 Typography Rules
- Maximum line length
- Heading hierarchy rules
- When to use bold / medium / regular

## 4. Spacing & Layout

### 4.1 Spacing Scale
Base unit: 4px or 8px  
Full scale (0.5, 1, 1.5, 2, 3, 4, 5, 6, 8, 10, 12, 16…).

### 4.2 Layout
- Max content width
- Breakpoints (mobile, tablet, desktop, wide)
- Grid or common layout patterns
- Container padding rules

## 5. Elevation, Borders & Radius

### Border Radius Scale
| Token     | Value    | Usage                |
|-----------|----------|----------------------|
| radius-sm | 4px      | …                    |
| radius-md | 8px      | …                    |
| radius-lg | 12px     | …                    |
| radius-full | 9999px | Pills, avatars     |

### Shadows / Elevation
Define 2–4 elevation levels with exact CSS values for light and dark mode.

### Borders
Border width and color tokens.

## 6. Component Guidelines (High-Level)
For the most important components, define:

#### Buttons
- Variants (primary, secondary, ghost, destructive)
- Sizes (sm, md, lg)
- States (default, hover, focus, active, disabled, loading)
- Icon + text rules
- Do’s and Don’ts

#### Form Elements (Input, Select, Checkbox, etc.)
- Anatomy
- States
- Error & help text treatment
- Label positioning

#### Cards / Panels
- Padding
- Elevation usage
- Header / footer patterns

#### Modals / Dialogs
- Sizes
- Overlay behavior
- Focus trapping expectations

#### Navigation
- Top bar / sidebar patterns
- Active state treatment

(Add other key components as needed: Toast, Badge, Avatar, Table, Tabs, etc.)

## 7. Iconography
- Preferred icon library (Lucide, Heroicons, Phosphor, custom, etc.)
- Size scale (16, 20, 24, 32…)
- Stroke width
- Color rules (currentColor preferred)
- When to use filled vs outline

## 8. Motion & Interaction
- Duration scale (150ms, 200ms, 300ms…)
- Easing recommendations
- What should animate and what should not
- Reduced motion preferences

## 9. Accessibility Requirements
- Minimum contrast ratios
- Focus ring style and visibility
- Keyboard navigation expectations
- Screen reader labels
- Touch target minimum size (44×44px)
- Color is never the only indicator

## 10. Implementation Notes for Developers & AI
- How design tokens should be organized in code (CSS variables, Tailwind config, theme file)
- Naming convention for tokens
- Dark mode implementation approach (class, media, or data attribute)
- Preferred way to apply styles (utility classes vs CSS modules vs etc.)
- File location for the design tokens / theme

## 11. Design Debt & Future Improvements
List known limitations of the current design system that may be addressed later.

---

# Quality Criteria
- Every color, size, and radius has a concrete value
- Type scale is complete and consistent
- Component guidelines cover the main states
- Accessibility is not an afterthought
- An AI agent should be able to create a new screen that looks coherent with the rest of the product using only this document

# Output Instructions
1. Output only the final Markdown of Design.md.
2. Start with:
   `<!-- Design system source of truth. AI must follow these tokens and rules when generating UI. -->`
3. Use tables extensively for scales and tokens.
4. Provide real hex values and rem/px values — never leave placeholders like “choose a blue”.
5. If brand colors were not provided, choose a modern, accessible palette and state that it is a proposed default.

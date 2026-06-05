# HTML Effectiveness Example Patterns

The source gallery contains twenty standalone HTML files. Treat them as pattern references: copy the structure, not the fictional Acme content.

Examples can be viewed in `references/examples`

## Pattern catalog

| Source file | Category | Reusable structure | Use when |
|---|---|---|---|
| `01-exploration-code-approaches.html` | exploration/planning | 3 approaches, code snippets, pro/con lists, metric badges, recommendation | comparing implementation choices |
| `02-exploration-visual-designs.html` | exploration/design | multiple visual directions rendered live with tone/density tradeoffs | choosing a UX/design direction |
| `16-implementation-plan.html` | planning/handoff | effort cards, milestones, data-flow diagram, mockups, key code, risks, open questions | handing implementation to another agent/engineer |
| `03-code-review-pr.html` | code review | PR summary, risk map, annotated diff, severity labels, next steps | reviewing a PR or patch |
| `17-pr-writeup.html` | code review/comms | motivation, before/after, file-by-file walkthrough, review focus, test plan, rollout | preparing a PR description for reviewers |
| `04-code-understanding.html` | code understanding | architecture summary, request path, callstack walkthrough, source snippets, key files, gotchas | explaining unfamiliar code or subsystem |
| `05-design-system.html` | design | token swatches, typography scale, spacing/radius/elevation, component examples | extracting/communicating design-system references |
| `06-component-variants.html` | design | variant matrix, controls for density/border/shadow, prop preview | reviewing component states or variants |
| `07-prototype-animation.html` | prototype | single interaction, easing controls, keyframe timeline, copy-paste CSS | tuning animation or motion feel |
| `08-prototype-interaction.html` | prototype | throwaway interaction, decision notes, open questions | feeling a UX flow before porting to production code |
| `10-svg-illustrations.html` | diagrams | inline SVG figure sheet, palette/rules, standalone export | producing docs/blog illustrations |
| `13-flowchart-diagram.html` | diagrams | process flowchart, click-to-inspect steps, pass/fail paths | explaining workflows, pipelines, or decision trees |
| `09-slide-deck.html` | deck | section-based slides, arrow-key navigation, compact metrics and decision slide | meeting-ready update or short presentation |
| `14-research-feature-explainer.html` | research/explainer | TL;DR, files read, step-by-step path, config/code tabs, gotchas, FAQ | explaining how a feature works from code/docs |
| `15-research-concept-explainer.html` | research/learning | interactive model, comparison table, glossary | teaching a concept with live parameters |
| `11-status-report.html` | report | metric cards, highlights, shipped table, velocity chart, carryover | recurring status updates |
| `12-incident-report.html` | report | TL;DR, timeline, root cause, impact metrics, action items | incident/postmortem writeup |
| `18-editor-triage-board.html` | custom editor | draggable cards, Now/Next/Later/Cut buckets, filters, copy as Markdown | prioritizing tickets, feedback, tests, ideas |
| `19-editor-feature-flags.html` | custom editor | form editor, dependency warnings, pending diff, copy full/diff | editing structured config safely |
| `20-editor-prompt-tuner.html` | custom editor | editable template, highlighted slots, live previews, token/char count, copy prompt | tuning prompts/templates/copy against examples |

## Structural recipes

### Exploration grid

Use when the user is uncertain. Create 3-6 options with:

- Title + one-sentence thesis
- Live rendering or concrete code
- Tradeoffs, not just pros
- A compact score row if useful: effort, risk, reuse, performance, accessibility
- Recommendation and conditions that would change it

### Annotated review

Use when the user needs judgment on code or a PR:

- Summary of what changed
- Risk map by file/module
- Annotated diff or file cards
- Severity labels: blocking, worth a look, nit, safe
- Suggested next steps and exact lines/files

### Handoff plan

Use when another agent/person will implement:

- Scope and non-goals
- Timeline/milestones split into independently reviewable slices
- Data flow or system diagram
- Mockups or interface examples
- Key code/schema snippets
- Risk table with mitigations
- Open questions with owners/timing

### Research explainer

Use when the goal is understanding:

- TL;DR first
- Files/data read
- Request path or concept path
- Expandable sections for detail
- Code/config snippets placed near explanations
- Gotchas and FAQ
- Glossary for terms that block comprehension

### Custom editor

Use when text prompts are a bad interface:

- Preload the data/options
- Use controls matching the work: drag/drop, toggles, sliders, textareas, tabs
- Validate constraints visibly
- Show pending changes
- Include export: copy markdown, copy JSON, copy diff, or copy prompt

# HTML Effectiveness Principles

Source basis: Anthropic's “Using Claude Code: The unreasonable effectiveness of HTML” and the `anthropics/html-effectiveness` example gallery.

## Why HTML beats Markdown for certain outputs

Use HTML when the answer needs one or more of these advantages:

1. **Information density:** tables, CSS, SVG, diagrams, code snippets, interactions, positioned layouts, and images can coexist in one readable surface.
2. **Visual clarity:** long specs and plans become navigable through cards, tabs, anchors, grids, timelines, and diagrams.
3. **Sharing:** a single file can be opened in a browser and passed around without a build step.
4. **Two-way interaction:** sliders, toggles, drag/drop, live previews, and copy buttons let the user refine choices instead of describing every tweak in text.
5. **Data ingestion:** when code, tickets, logs, docs, or research have been read, HTML can expose the shape of that context rather than dumping a summary.

## HTML selection test

Choose HTML if any answer is “yes”:

- Would the reader compare multiple options side by side?
- Would a diagram, timeline, diff, matrix, or map reduce cognitive load?
- Would the user skim a long Markdown document but read a visual page?
- Does the user need to tune values by feel: colors, easing, priorities, prompt variables, config flags?
- Would a copy/export button make the next step easier?
- Does the artifact need to be shared with someone who will not read a long chat transcript?

Stay in Markdown if the output is under about a page, purely textual, or expected to be pasted into a plain-text destination.

## Design principles

- **Purpose before polish:** each visual element must answer “what can the reader see faster because of this?”
- **One artifact, one job:** exploration page, PR review, incident report, and editor are different shapes; do not merge them unless the user asks.
- **Reader path:** put TL;DR and navigation near the top; deep details later or behind toggles.
- **Side-by-side beats serial prose:** comparisons should be visible at once, not separated by pages of text.
- **Inline provenance:** show files read, assumptions, prompt/source, or generated date when relevant.
- **Export closes the loop:** any interactive editing surface must produce copyable output.
- **No unnecessary stack:** no React/Vite/Tailwind/CDN unless the user explicitly asks or the environment demands it.

## Anti-patterns

- “HTML maximalism”: using HTML for a short answer with no visual or interactive value.
- “Decorated Markdown”: wrapping a linear essay in a page without adding structure.
- “Screenshot thinking”: visual output that cannot be copied, inspected, or reused.
- “Dead-end editor”: a UI that lets the user make choices but does not export them.
- “External dependency drift”: a supposedly portable file relying on unavailable scripts, fonts, or images.
- “Fake certainty”: metrics, source references, or code paths invented because the artifact format feels authoritative.

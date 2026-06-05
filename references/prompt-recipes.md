# Prompt Recipes

Use these recipes when the user wants help asking another agent to create HTML-effective outputs.

## Generic request

```text
Create a single self-contained HTML file, not Markdown. Optimize it for [reader] to [decision/action]. Use inline CSS/JS/SVG only, no external dependencies. Include [sections]. Make it responsive and easy to skim. If any values are editable, include a copy/export button that outputs [format].
```

## Explore implementation approaches

```text
Generate 3-5 distinct implementation approaches for [problem]. Put them side by side in a single self-contained HTML file. For each approach show the core code shape, pros/cons, effort, risk, testability, and when it would be the right choice. End with a recommendation and what evidence would change it.
```

## Implementation plan

```text
Create a thorough implementation plan as a single HTML file. Include scope/non-goals, milestones, data flow, mockups or interface sketches, key code/schema snippets, risk table with mitigations, test plan, rollout plan, and open questions. Make it easy for another engineer or agent to execute without rereading this conversation.
```

## PR review artifact

```text
Help me review this PR by creating a self-contained HTML artifact. Summarize what changed, render the important diffs with inline margin annotations, color-code findings by severity, include a file risk map, and end with exact next steps. Focus on [area of concern].
```

## PR writeup for reviewers

```text
Write an HTML PR description for reviewers. Explain the motivation, before/after behavior, file-by-file walkthrough ordered for comprehension, where reviewers should focus, test plan, rollout plan, and what was intentionally left out.
```

## Codebase explainer

```text
Read the relevant files for [feature/subsystem] and produce a single HTML explainer page. Include a TL;DR, files read, request/data path diagram, key code snippets annotated in context, gotchas, and FAQ. Optimize for someone who will read it once and then modify the code.
```

## Design exploration

```text
Generate [number] different visual directions for [screen/component]. Render each live in one HTML file so I can compare layout, tone, density, accessibility, and light/dark behavior. Label the tradeoff each direction makes.
```

## Motion/interaction prototype

```text
Create a throwaway self-contained HTML prototype for [interaction]. Include controls for [duration/easing/state/options], let me try the interaction, explain what design decisions are baked in, and add a copy button for the chosen parameters/CSS.
```

## Status or incident report

```text
Create a self-contained HTML report from [sources]. Put the TL;DR and key metrics at the top, then use a timeline/table/chart to show details. Include shipped/slipped/blocked or root-cause/impact/action-items as appropriate. Show sources and assumptions.
```

## Custom editor

```text
Build a one-off HTML editor for [data/task]. Preload the current data, add controls that match the task, validate constraints visibly, show pending changes, and include a button to copy the result as [JSON/Markdown/diff/prompt]. This is a throwaway decision surface, not a production app.
```

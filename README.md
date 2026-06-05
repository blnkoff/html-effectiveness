# HTML Effectiveness Skill for AI Agents (`agentskills` format)

An advanced, production-ready portable skill for AI agents, built strictly according to the open [Agent Skills Specification](https://agentskills.io). 

This skill directly implements and scales the core philosophy shared by Tariq in his seminal essay **"Using Claude Code: The Unreasonable Effectiveness of HTML"**. It shifts the AI agent paradigm from outputting flat, text-heavy Markdown responses to generating rich, standalone, interactive HTML interfaces. 

Once added to an agent's workspace, the agent autonomously uses this skill's instructions, validation tooling, and 20+ reference patterns to render operational dashboards, visual code explorations, design systems, and responsive prototypes directly from the CLI.

> **Inspiration & Attribution:** This framework is built around the insights shared by Tariq ([@trq212](https://x.com/trq212)), Engineer at Anthropic, demonstrating that HTML is vastly superior to Markdown for complex agentic outputs, inline UI previews, and multi-step diagnostic reports.

---

## ⚙️ How It Works (Progressive Disclosure)

Compatible AI clients (such as Claude Code, Roo Code, Goose, OpenHands, etc.) leverage this skill in three lifecycle stages:
1. **Discovery:** At startup, the agent indexes the metadata in `SKILL.md` to understand when this HTML rendering capability is relevant.
2. **Activation:** When a user task requires rich documentation, UI prototyping, or deep code analysis, the agent loads the full instructions into its context window.
3. **Execution:** The agent leverages the bundled scaffolding scripts, standard assets, and example patterns to compile structural data into isolated HTML artifacts.

---

## 📂 Skill Architecture

This repository follows the standard `agentskills` structure, making it fully portable across compliant ecosystem clients:

```text
.
├── SKILL.md                        # REQUIRED: Main entry point containing agent metadata & execution instructions
├── agents/
│   └── openai.yaml                 # Core system prompts and schema definitions for LLM clients
├── assets/
│   └── starter-html-artifact.html  # Base HTML/Tailwind skeleton used by agents to scaffold new outputs
├── references/
│   ├── html-effectiveness-principles.md # Core architectural guidelines adapted from Tariq's essay
│   ├── prompt-recipes.md           # Injectable prompt blocks forcing the agent into HTML mode
│   ├── quality-checklist.md        # Strict validation criteria used by the agent to self-correct
│   ├── example-patterns.md         # Design patterns mapping complex tasks to UI components
│   └── examples/                   # 20 pre-built reference implementations for agent context
│       ├── 01-04/                  # Code exploration, structural understanding, and visual PR reviews
│       ├── 05-10/                  # Component variants, design systems, animations, and interactive prototypes
│       ├── 11-17/                  # Incident reports, status tracking, flowcharts, and implementation plans
│       ├── 18-20/                  # Advanced triage boards, feature flags, and prompt-tuning sandboxes
│       └── index.html              # Central preview gallery for all generated artifacts
└── scripts/
    ├── check_html_artifact.py      # Automated Python suite for agents to validate output compliance
    └── new_html_artifact.py        # CLI tool used by agents to programmatically scaffold new canvases
```

---

## 🛠️ Automated Agentic Workflows

When activated, this skill guides the agent to abandon wall-of-text console logs and instead build self-contained web interfaces containing embedded CSS/JS. Key automated capabilities include:

* **Codebase Navigation & Review:** The agent renders rich, visual pull request writeups (`17`), interactive code triaging maps (`18`), and functional design system sandboxes (`05`).
* **Interactive Operations & Diagnostics:** The agent generates dynamic incident post-mortems (`12`), visual engineering flowcharts (`13`), and feature flag management dashboards (`19`).
* **Autonomous Quality Gates:** Before finalizing any artifact, the agent is instructed to run `scripts/check_html_artifact.py` to programmatically ensure the generated code satisfies layout constraints, responsive design tags, and has zero broken script tags.

---

## 🚀 Installation & Ecosystem Usage

To dynamically inject this capability into your Agent Skills compatible environment, run the installation command inside your agent's workspace or global project root:

```bash
npx skills add blnkoff/html-effectiveness

```

Once installed, compatible agents will automatically discover the skill and deploy it whenever a user requests complex data structures, operational reviews, mockups, or comprehensive technical plans.

---

## 📖 References & Acknowledgements

* **Author:** Tariq ([@trq212](https://x.com/trq212)), Engineer at Anthropic.
* **Original Essay:** ["Using Claude Code: The Unreasonable Effectiveness of HTML"](https://x.com/trq212/status/2052809885763747935) — the foundational deep-dive exploring why native web technologies unlock the true potential of interactive AI agent outputs.
* *Special thanks to Tariq for pioneering and articulating this paradigm shift. This repository serves as an extended, ready-to-use Agent Skill built entirely around that vision.*

---

## 📄 License

This framework is open-source and available under the MIT License.
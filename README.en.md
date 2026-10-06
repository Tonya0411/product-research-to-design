# product-research-to-design

[![中文](https://img.shields.io/badge/%E4%B8%AD%E6%96%87-red.svg)](README.md) [![English](https://img.shields.io/badge/English-blue.svg)](README.en.md)

> GitHub repo: <https://github.com/Tonya0411/product-research-to-design>

A general-purpose "research → design delivery" skill for product / industrial design projects: takes you from user & market research all the way to a PRD and a design brief.

## What this is

A reusable research workflow skill that bundles two methodology guides plus a blank project-baseline template. It is not a case library tied to any single product — it is a standard process most of the product / industrial design project can follow.

## Directory structure

```
product-research-to-design/
├── SKILL.md                  # Main skill file: triggers + 7-step flow + 3 hard rules
├── README.md / README.en.md  # This guide (Chinese / English)
└── references/
    ├── methodology/
    │   ├── Survey_method.md        # Questionnaire design methodology
    │   └── Investgation_method.md  # Design research methodology (PSTP, primary + secondary)
    └── templates/
        └── 项目基线空白模板.md       # Blank project baseline to fill in first
```

## When to use

- To run user research or design a questionnaire for a new/existing product
- To do secondary + primary research, cross-analysis, and surface insights & opportunities
- To write a research synthesis report, PRD, or design brief
- To reuse a standard "research → design" process and deliverable format

## Quick start (three steps)

1. **Fill the baseline**: copy `references/templates/项目基线空白模板.md` into your project folder and fill in product, target users, business constraints, confidentiality constraints, and research goals.
2. **Run the flow**: follow the seven steps in `SKILL.md` — questionnaire → secondary research → primary research → cross-analysis → design brief → PRD.
3. **Produce deliverables**: six outputs (questionnaire, secondary research checklist, primary data notes, synthesis report, design brief, PRD).

## Detailed usage (the seven-step flow)

| Step | What you do | Key points | Deliverable |
|---|---|---|---|
| 0 Baseline | Fill `项目基线空白模板.md` | Lock product / users / price / confidentiality / goals | Project baseline |
| 1 Questionnaire | Write questions per the survey methodology | ≤20 questions, mostly closed, funnel ordering, no spoilers, attention check | .txt importable into 问卷星 |
| 2 Secondary research | PSTP five-drawer research | Set D1–D4 goals before searching; A/B/C/D credibility tiers | Industry understanding + checklist |
| 3 Primary research | Collect and organize survey data | Check sample size, attention-check pass rate, cross-tabs | Primary data notes |
| 4 Cross-analysis | Triangulate primary × secondary | Insights backed by both sources; tiered opportunities | Synthesis report |
| 5 Design brief | Persona / scenario / features / constraints / guardrails / acceptance | Features split into required / optional | Design brief |
| 6 PRD | Write the PRD per the pm-skills framework | Model outputs require an AI Behavior & Evaluation section | PRD |

## Three hard rules

1. **Never fabricate data**: quantitative figures must come from research documents; mark anything missing as 【资料无记录】.
2. **Never leak the design concept**: use neutral wording in outward-facing materials (questionnaires, interview guides) so you do not prime respondents.
3. **Trace every number**: label conclusions and charts with their source (【primary Q#】 / 【secondary】).

## Installation

### Option 1: DSH skills directory (local)

Copy the whole `product-research-to-design` folder into the user-level skills directory:

```powershell
# Windows PowerShell
Copy-Item -Recurse -Force `
  "C:\path\to\product-research-to-design" `
  "C:\Users\<YourUserName>\.agents\skills\product-research-to-design"
```

After installing, `product-research-to-design` will appear in DSH's available skills list.

### Option 2: skills CLI (cross-tool / share via GitHub)

Hosted on GitHub — install via the skills ecosystem:

```bash
npx skills add Tonya0411/product-research-to-design -g -y
```

## How to invoke it in DSH

When starting a new project, tell the assistant:

> Use the product-research-to-design skill to help me do user research and a PRD for [some product].

The assistant will ask you to fill the project baseline first, then walk through the seven steps.

## Relationship to pm-skills

The PRD step follows the `deliver-prd` skill framework (v3.0.0) from GitHub [`product-on-purpose/pm-skills`](https://github.com/product-on-purpose/pm-skills). When a product's output comes from an LLM, the PRD must include the "AI Behavior and Evaluation" section (refusal / abstention / privacy each on their own row, with thresholds).

## FAQ

**Q: Can I skip the questionnaire and start with secondary research?**
A: Yes. The seven steps are a recommended order; if secondary material already exists, do Step 2 first and defer Steps 1 and 3 as needed.

**Q: Does it work for non-AI hardware (no LLM output)?**
A: Yes. Per pm-skills convention, the "AI Behavior" section in Step 6 can be skipped; the rest of the flow applies as-is.

**Q: How do I fill the confidentiality constraint?**
A: If the form factor is confidential, use neutral wording in outward materials (e.g., "desktop companion device") and record the concept to hide in the template's confidentiality field.

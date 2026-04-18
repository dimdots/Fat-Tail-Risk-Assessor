# Fat-Tail Risk Assessor

A structured risk assessment tool for IT and AI projects, built as a Claude Project. Grounded in Bent Flyvbjerg's research on fat-tailed project risk.

## What this is

Most project risk analysis assumes things go a little over budget, a little over schedule. Flyvbjerg's data — 16,000+ projects across 136 countries — shows that certain project types don't follow that pattern. They follow fat-tailed distributions: most projects look fine, but a small percentage produce catastrophic overruns that destroy budgets, careers, and companies.

IT sits at the top of that list. In Flyvbjerg's [2026 peer-reviewed paper](https://doi.org/10.1177/87569728241311009) (Project Management Journal, Vol. 57(1), 14-43), IT is ranked the single most fat-tailed project type across 11,011 projects in 23 categories. It is the only category where the statistical distribution implies no finite worst case.

This tool helps project leaders pressure-test their IT and AI initiatives against that research before committing budget and reputation.

## What's in the repo

| File | Purpose |
|------|---------|
| `01_system_instructions.md` | The system prompt — paste into your Claude Project's instructions field |
| `02_framework_knowledge.md` | The analytical framework — upload as a project knowledge file |
| `03_test_cases.md` | Five test cases to validate your setup covers real-world scenarios |
| `04_setup_guide.md` | Step-by-step guide to get running in ~30 minutes |

## How it works

You describe a project. The tool assesses it against 10 fat-tail risk factors (modularity, bespokeness, novelty, "think-fast" commitment, duration, scope clarity, stakeholder complexity, political exposure, dependency complexity, feedback loop speed) plus 7 AI-specific risk factors. It produces a structured report: risk classification, the specific factors driving it, what to watch, and questions to ask the sponsor.

The output reads like a senior PM looked at your specific situation — not like a model ran a checklist.

## What you need

- A Claude Pro or Team subscription
- 30 minutes to set up and run the first test
- 2-3 hours to run all five test cases and iterate

## The framework

The risk framework is built on two layers:

**Fat-tail risk factors** (from Flyvbjerg's research): modularity, bespokeness, novelty, "think-fast" commitment, duration, scope clarity, stakeholder complexity, political/reputational exposure, dependency complexity, and feedback loop speed. These apply to any IT project.

**AI-specific risk factors**: data quality and availability, model uncertainty, success metric clarity, change management scope, governance and regulatory exposure (including EU AI Act, high-risk system requirements effective August 2, 2026), vendor lock-in and model drift, and organizational readiness. These apply when the project involves AI/ML components.

The tool classifies projects as Low, Moderate, High, or Severe — but the real value is in the specific factors and the questions it surfaces, not the label.

## Customize it

The system prompt ships with a specific PM persona. Change it to match your background. The more specific you make it, the less the output sounds like a generic AI assistant.

The framework knowledge document is designed to be extended. If your industry has specific risk factors (e.g., GxP validation in pharma, FINMA requirements in Swiss banking), add them.

## Background

This tool was built as part of a series exploring how project managers can use AI to improve delivery practices — specifically by applying Flyvbjerg's "think slow" principle: structured deliberation before commitment.

It is not a replacement for experienced project leadership. It is a structured pause — a way to surface the questions that should be asked before the money moves.

## Credits

The analytical foundation comes from the work of Professor Bent Flyvbjerg, particularly:

- Flyvbjerg, B. & Gardner, D. (2023). *How Big Things Get Done: The Surprising Factors That Determine the Fate of Every Project, from Home Renovations to Space Exploration and Everything In Between*. Currency.
- Flyvbjerg, B., Budzier, A., Lee, J.S., Kapsali, M., & Negrea, O.D. (2026). The Uniqueness of IT Cost Risk: A Cross-Group Comparison of 23 Project Types. *Project Management Journal*, 57(1), 14-43.

Built by [Dmytro Dotsenko](https://www.linkedin.com/in/dmytro-dotsenko/) — senior PM and delivery lead, 17+ years in complex project delivery.

## License

This framework is shared freely. Use it, adapt it, build on it. If you publish something based on it, a mention is appreciated.

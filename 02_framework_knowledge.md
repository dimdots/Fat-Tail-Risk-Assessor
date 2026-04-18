# Fat-Tail Risk Framework — Reference Document

This document is attached to the Claude Project as knowledge. The model uses it as its analytical foundation when assessing projects.

## The Core Insight (Flyvbjerg)

Most project risk analysis assumes normal distributions — projects overrun by small, predictable amounts. This is wrong for many project categories. Flyvbjerg's research shows that certain project types follow fat-tailed distributions: the average overrun may look manageable, but the upper tail produces rare catastrophic blowups that destroy companies, careers, and political reputations.

Two datasets inform this framework:

1. **"How Big Things Get Done" (2023):** 16,000+ projects across 25 categories, 136 countries. IT ranked #4 on the fat-tail risk list, behind nuclear waste storage, the Olympics, and nuclear power plants.

2. **"The Uniqueness of IT Cost Risk" — Flyvbjerg et al., Project Management Journal, Vol. 57(1), 14-43 (2026):** 11,011 projects across 23 categories in 126 countries. **IT is now ranked #1 — the most fat-tailed project type in the dataset.** IT is the only category with a Pareto tail parameter α ≤ 1 (α = 0.92), which in statistical terms means the cost overrun distribution has no finite mean and no finite variance. Worst-case scenarios are effectively unbounded.

The least fat-tailed (safest) project types share one attribute: **modularity**. You build many small identical units. If one unit fails, the others still work. Solar power, wind power, transmission lines, and roads sit at the safe end of the spectrum.

The most fat-tailed (riskiest) project types share the opposite attribute: **"one huge thing"**. Everything must work together at full scale for anything to work at all.

## The IT "Barbell" Risk Profile

IT risk does not behave like other fat-tailed categories. It is a barbell:

- **Only ~41% of IT projects overrun at all** (vs. 97% for nuclear power, 100% for the Olympics). On the surface, IT looks safer.
- **When IT projects do fail, the average overrun is ~453%.** The failures are catastrophic and rare, not common and moderate.

This matters for how assessments land. The sponsor's prior is likely "most of our IT projects turn out fine" — and statistically that is correct. The job of a risk assessor is not to predict failure but to identify whether *this specific project* has the attributes that put it in the catastrophic tail rather than the benign middle.

Flyvbjerg's 2026 paper names two root causes for IT's uniqueness:

- **Bespokeness:** Almost every enterprise IT project is a custom build, which defeats the modularity that protects other categories. Each new project starts at zero rather than assembling proven components.
- **"Think-fast" decision making:** The temptation to commit before the problem is truly understood, because software feels malleable in a way that concrete does not. Reversibility is assumed and turns out to be false.

The proposed antidotes are specific: **modularity** where possible, and **"think slow"** before the money moves. This tool exists to support the second.

## Fat-Tail Risk Factors

When assessing a project, evaluate exposure to these factors:

### 1. Modularity
**Low modularity = high fat-tail risk.** Can this project ship in pieces that deliver value independently, or must the whole thing be built before anything works? A 10-site rollout of identical ATMs is modular. A single enterprise ERP is not. Modularity is the single strongest protective factor in Flyvbjerg's data.

### 2. Bespokeness
**Custom build = high fat-tail risk.** Is this project assembling proven, previously-used components, or is each major piece being designed from scratch for this specific organization? Bespokeness is the attribute Flyvbjerg isolated in 2026 as the reason IT moved to #1. "We're doing it our way because our business is unique" is the sound of the fat-tail filling with risk.

### 3. Novelty
**Novel technology = high fat-tail risk.** Has this specific thing been built successfully before, with this kind of team, in this kind of organization? Novelty multiplies unknowns. Distinct from bespokeness: novelty is "new to the world," bespokeness is "new to us."

### 4. "Think-fast" commitment
**Pre-commitment without structured deliberation = high fat-tail risk.** Did the sponsor decide to go before the problem was fully scoped, on the assumption that "we can figure it out as we go"? Software's apparent malleability makes this failure mode specifically dangerous in IT. Reversibility is usually assumed and usually false.

### 5. Duration
**Longer timeline = higher fat-tail risk.** Every additional month is another month for scope to drift, sponsors to leave, requirements to change, and black swans to materialize. Flyvbjerg's research is clear: shorter projects survive.

### 6. Scope clarity
**Vague scope = high fat-tail risk.** "Modernize our systems" is a fat-tail bet. "Replace the customer onboarding flow with version X" is not. IT projects are especially exposed here because the material is digital, so there's no physical constraint forcing scope discipline.

### 7. Stakeholder complexity
**More decision-makers with unclear alignment = higher risk.** Projects fail when a key stakeholder changes their mind at month 14, not when the tech breaks.

### 8. Political/reputational exposure
**High visibility = asymmetric downside risk.** Projects that cannot be allowed to fail publicly often end up failing expensively because leaders double down rather than course-correct.

### 9. Dependency complexity
**More external dependencies = higher fat-tail risk.** Third-party vendors, data migrations, regulatory approvals, integrations — each one is a potential cascade trigger.

### 10. Feedback loop speed
**Slow feedback loops = higher fat-tail risk.** IT projects are particularly bad here. Problems often surface months after the decisions that caused them, making correction expensive.

## AI-Specific Risk Factors

AI projects inherit all the IT project risks above, plus these additional ones:

### A. Data quality and availability
Most AI projects discover too late that their data is insufficient, dirty, biased, or legally constrained. If the user has not explicitly addressed data readiness, this is a major risk.

### B. Model uncertainty
AI systems are probabilistic. "Done" is not binary. A model that performs at 85% accuracy on test data may fail silently at 70% in production. Success metrics must be defined in business terms, not just model metrics.

### C. Success metric clarity
Many AI projects have vague success definitions ("improve customer experience", "better decisions"). Without quantified, measurable, pre-agreed metrics, benefit realization is impossible to claim.

### D. Change management scope
The technology is rarely the hard part. Getting humans to trust, use, and integrate AI outputs into existing workflows is where most projects stall. If change management is not explicitly budgeted as at least 30% of the project cost, red flag.

### E. Governance and regulatory exposure
For projects touching EU residents or EU markets, the EU AI Act's high-risk system requirements come into force on 2 August 2026. Switzerland is developing its own framework. Projects without governance planning are exposed to both compliance risk and downstream liability.

### F. Vendor lock-in and model drift
AI vendors change pricing, models deprecate, APIs shift. A production system built on last year's best model may need to be rebuilt. This is rarely budgeted for.

### G. Organizational readiness
Organizations that have never shipped production AI before tend to underestimate the operational work: MLOps, monitoring, retraining, human oversight. This is the difference between a proof-of-concept that impresses executives and a production system that actually works.

## Severity Scale

For IT and AI projects, remember the barbell: ~41% of IT projects do not overrun at all. The point of the scale is not to predict whether *this* project will fail — it is to identify whether the project has the structural attributes that put it at risk of landing in the catastrophic tail.

- **Low:** Few fat-tail factors apply. Project has modular structure, clear scope, mature technology, short timeline, proven vendor configuration. The structural profile is on the benign side of the barbell. Overruns, if any, likely stay within ~20%.
- **Moderate:** Two or three fat-tail factors apply, but none are severe. Manageable with disciplined delivery practices and disciplined scope control.
- **High:** Four or more fat-tail factors apply. Project is in fat-tail territory. Credible outcomes include overruns of 50-200%. Requires active risk governance, real sponsor air cover, and a structured pre-commitment review.
- **Severe:** Project hits most fat-tail factors — low modularity, high bespokeness, novel tech, "think-fast" commitment, long timeline, vague scope, high political stakes. These are the projects that produce 400%+ overruns and career-ending failures (the 2026 data puts the IT tail-failure average at 453%). The responsible call is to reconsider scope, sequencing, or go/no-go before proceeding.

## How to deliver assessments

When producing a risk report, be specific to the project described. Do not recite this framework — apply it. The user should feel that a senior PM looked at their specific situation, not that a model ran a checklist.

Lead with the structural pattern, not the checklist. "This project is bespoke, long-duration, and non-modular — that puts it in the same structural category as the IT projects that produce 450%+ overruns" is useful. "You scored 7 out of 10 on the risk factors" is not.

The tool's purpose is to support "think slow" before the money moves. A good assessment slows the sponsor down at the right moment, points at the specific decisions that deserve more scrutiny, and makes it harder — in a good way — to commit on optimism alone.

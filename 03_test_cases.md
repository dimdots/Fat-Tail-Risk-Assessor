# Test Cases — Validate the Tool

Run these test cases once the Claude Project is set up. Each one is designed to expose a specific kind of weakness in the tool. If it handles all five well, you're ready to move to the next stage.

Use these as the first message you send into the Project. Note what the tool does well and what it misses.
You can use projects from your own practice, where you already know the outcomes
---

## Test Case 1: The obviously severe project

"We're a Swiss pharmaceutical company planning to replace our legacy ERP with a custom-built AI-augmented system that will handle manufacturing, finance, and regulatory reporting across 14 sites in 8 countries. The timeline is 36 months. Budget is CHF 45 million. We're partnering with a consulting firm that has done large ERP projects but not with AI augmentation. Go-live is a single global cutover."

**Expected behavior:** Tool should classify this as Severe. Should flag low modularity, novel AI augmentation, long duration, high regulatory exposure, single cutover, vendor/consultant novelty. Should ask sharp questions about staged rollout, data readiness, and change management budget.

**What to watch for:** Does it actually push back, or does it hedge? A soft response here means the system prompt needs tightening.

---

## Test Case 2: The genuinely low-risk project

"We're rolling out a pre-built HR onboarding tool from a vendor we already use to 6 office locations in Switzerland. Each site is essentially identical. Budget is CHF 80,000. Timeline is 3 months with one pilot site first. The vendor has deployed this exact configuration for 200+ customers."

**Expected behavior:** Tool should classify this as Low. Should note high modularity, mature technology, short timeline, clear scope, low stakeholder complexity. Should not manufacture concerns.

**What to watch for:** Does it resist the urge to always find problems? An AI tool that says everything is risky is useless.

---

## Test Case 3: The AI project with hidden data problems

"We want to build an AI model to predict customer churn for our B2B software company. We have 8 years of CRM data. Budget is $300K, timeline is 6 months. We want to deploy it to our sales team to help them prioritize accounts. Success means improving retention by 5%."

**Expected behavior:** Tool should ask about data quality and labeling, the definition of "churn" in the CRM, how the 5% retention lift will be measured and attributed, change management for the sales team, model drift over time, and whether 6 months is enough for the full lifecycle. Should land in High territory, driven by success metric attribution and change management risk.

**What to watch for:** Does it engage with the AI-specific risks seriously, or does it just apply the generic IT framework?

---

## Test Case 4: The deliberately under-described project

"We want to use AI to transform our operations."

**Expected behavior:** Tool should refuse to assess. Should ask a focused batch of clarifying questions covering what specifically is being built, budget, timeline, organization, and existing AI maturity. Should not produce a risk assessment based on nothing.

**What to watch for:** Does it hallucinate an assessment, or does it correctly hold the line and ask for more? Holding the line is the right behavior.

---

## Test Case 5: The politically sensitive public-sector project

"A Swiss cantonal government wants to deploy a facial recognition system at major train stations for security purposes. Budget is CHF 12 million. Timeline is 18 months. The tech is based on a vendor's off-the-shelf model adapted for the use case."

**Expected behavior:** Tool should flag severe governance and regulatory risk under EU AI Act (facial recognition in public spaces is prohibited or high-risk under Article 5 and Annex III), political/reputational exposure, public backlash risk, and data protection exposure. Should classify as Severe or High. Should recommend legal counsel, not just technical mitigation.

**What to watch for:** Does it engage with the regulatory and ethical dimension, or does it treat this as a purely technical project? A good senior PM would not touch this without legal clearance, and the tool should reflect that judgment.

---

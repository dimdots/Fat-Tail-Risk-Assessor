# Setup Guide — Up and Running in ~30 minutes

This walks you through turning the files in this folder into a working Claude Project you can test today.

## Prerequisites

- Claude Pro or Team subscription (ChatGPT could be used too)
- About 30 minutes

## Steps

### 1. Create the project

Open Claude (claude.ai). In the left sidebar, click "Projects" → "Create project".

- **Project name:** Fat-Tail Risk Assessor
- **Description:** Senior-PM-grade risk assessment for IT and AI projects, grounded in Flyvbjerg's fat-tail research.

### 2. Add the system instructions

Open `01_system_instructions.md`. Copy everything between the horizontal rules (the full system prompt). Paste it into the "Project instructions" field in Claude.

### 3. Attach the knowledge document

Upload `02_framework_knowledge.md` as a project file. This is what Claude references when analyzing projects.

You can also upload `flyvbjerg_fat_tails_chart.png` from the parent folder as a visual reference, though this is optional.

### 4. First test

In the project chat, paste Test Case 1 from `03_test_cases.md`. Read the response carefully. Does it feel like a senior PM wrote it, or does it feel like a generic AI assistant? Note anything that's off.

### 5. Run all five test cases

Run each test case in a fresh conversation within the project (important — fresh context each time). Keep a notes document with what worked and what didn't. These notes become content later.

### 6. Iterate the system prompt

If a test case produces weak output, the fix is almost always in the system prompt, not the knowledge document. Edit the instructions and re-run that test.

Common fixes:
- If the tool is too soft: add stronger language about being direct and willing to disagree
- If it hallucinates assessments with no data: strengthen the intake step
- If it produces generic output: add explicit instructions to tie every sentence to the specific project
- If the tone feels AI-generated: reinforce the "avoid these words" list

### 7. Customize

The system prompt uses a specific PM persona. Edit it to match your own background and style. The specificity is what makes the output feel human — a generic prompt produces generic assessments.

Things worth customizing:
- The persona description (your experience, industries, seniority level)
- The "avoid these words" list (add any AI-tell phrases that bother you)
- The output format (add or remove sections based on what your stakeholders need)

### 8. Scoring your v1

Once you have at least four of five test cases producing responses you'd be comfortable showing to a colleague or client, you have a working tool.


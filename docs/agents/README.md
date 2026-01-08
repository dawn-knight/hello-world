# Cursor Agents Game Dev Team Kit

This folder contains reusable role briefs and shared workflows for running a small-to-mid sized game development team using Cursor agents.

## How to use

- Pick a **project** and create a short spec (or paste an existing one) using `templates/task-brief.md`.
- Assign one or more roles from `roles/ROLE_INDEX.md`.
- For each agent, paste:
  - the relevant role brief (e.g. `roles/gameplay-programmer.md`)
  - the current task brief
  - any repo constraints (engine/tech stack, target platforms, performance budgets)
- Require every agent output to include:
  - **Deliverables** (files/sections produced)
  - **Assumptions**
  - **Risks / open questions**
  - **Next handoff** (use `templates/handoff.md`)

## Recommended folder conventions (optional)

These docs are tool-agnostic. If you want a predictable structure for agent outputs, add:

- `docs/game/`: GDD, TDD, narrative bible, UX flows
- `docs/art/`: style guide, palettes, silhouettes, export settings
- `docs/tech/`: architecture notes, build/release notes, perf budgets
- `docs/qa/`: test plans, known issues, repro steps

## What’s included

- `TEAM_CHARTER.md`: shared rules (Definition of Done, quality bars, handoffs)
- `WORKFLOWS.md`: planning → implementation → review → QA → release
- `roles/`: one file per role (definition, responsibilities, instructions)
- `templates/`: task briefs, handoffs, review checklists, prompt header


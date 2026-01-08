# Workflows (Planning → Build → Review → QA → Release)

This document defines repeatable workflows for agent-based collaboration.

## 1) Intake → Task brief

**Inputs**: goal, target platform(s), engine/stack, constraints, deadline.

**Output**: one task brief using `templates/task-brief.md`.

Rules:

- If requirements are unclear, record assumptions inside the brief instead of stalling.
- Define a measurable success signal (FPS, retention metric, “level completes in X minutes”, etc.).

## 2) Discovery → Risk register

**Owner**: Producer/Scheduler + Tech Lead.

Steps:

- List unknowns (tech feasibility, asset creation, scope).
- Identify dependencies between roles.
- Decide the smallest “vertical slice” that proves fun + feasibility.

**Output**: 5–15 bullets in the task brief under “Risks”.

## 3) Implementation → Vertical slice delivery

**Owner**: relevant role(s).

Steps:

- Work in small increments; keep changes reviewable.
- Provide a short test plan (how to verify the slice).
- Update docs when behavior/controls change.

**Output**:

- Code/assets/docs changes
- Handoff note using `templates/handoff.md`

## 4) Review → Merge readiness

**Reviewer**: peer role (e.g., gameplay ↔ tech lead; UI ↔ accessibility; art ↔ tech art).

Checklist:

- Meets DoD in `TEAM_CHARTER.md`
- No obvious performance regressions
- Edge cases considered
- Naming, file locations, and conventions respected

Use `templates/review-checklist.md`.

## 5) QA → Repro + regression

**Owner**: QA Lead.

Steps:

- Verify task acceptance criteria.
- Add repro steps for any issues found.
- Confirm fixes with “fixed in build/version” notes.

**Outputs**:

- `docs/qa/TEST_PLAN.md` updates (or brief test notes in handoff)
- Bug reports using `templates/bug-report.md` (optional)

## 6) Release → Build, notes, validation

**Owner**: Build/Release Engineer.

Steps:

- Produce a reproducible build.
- Validate on target platform(s).
- Write release notes and known issues.

**Outputs**:

- `docs/release/RELEASE_NOTES.md`
- `docs/release/KNOWN_ISSUES.md`
- version/build metadata

## 7) Retrospective → Improve the system

Questions:

- Where did we lose time? (handoffs, unclear specs, flaky builds)
- What quality bars were missing?
- What should be templated next?

Output:

- small edits to this kit (roles/templates/workflows), not a long memo.


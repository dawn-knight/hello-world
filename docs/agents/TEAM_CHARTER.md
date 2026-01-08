# Team Charter (Cursor Agents Game Dev Team)

This charter is the shared operating agreement for all roles and agents. Keep it stable; adapt per project by adding a `docs/game/PROJECT_BRIEF.md`.

## Principles

- **Ship small slices**: prefer vertical slices over big-bang milestones.
- **Make it testable**: every change should be verifiable (repro steps, test plan, build steps).
- **Document decisions**: record tradeoffs and rationale, not just outcomes.
- **Performance is a feature**: establish budgets early and defend them.
- **Accessible by default**: input, readability, color contrast, and motion sensitivity.

## Definition of Done (DoD)

Work is “done” only if:

- **Meets acceptance criteria** from the task brief.
- **No known regressions** introduced in touched areas.
- **Test plan included** (manual steps at minimum; automated tests when feasible).
- **Docs updated** if behavior, controls, or content changed.
- **Assets validated** (naming, formats, import settings, size budgets).
- **Handoff note written** using `templates/handoff.md`.

## Quality bars

- **Gameplay**: clear goal, readable feedback, fair failure, consistent controls.
- **UI/UX**: legible at target resolution, consistent navigation, controller-friendly if applicable.
- **Art**: style-consistent, correct scale/pivot/origin, optimized textures/meshes.
- **Audio**: not clipping, appropriate loudness, coherent spatialization (if used).
- **Code**: readable, deterministic where needed, minimal coupling, logs are actionable.
- **Build**: reproducible, versioned, documented, no “works on my machine” steps.

## Performance budgets (template)

Decide and record early (per platform):

- **Frame rate target** (e.g., 60fps) and acceptable lows.
- **CPU budget** per frame (ms), key systems budget (AI, physics, gameplay).
- **GPU budget** per frame (ms), key passes budget (shadows, post).
- **Memory budgets**: RAM, VRAM, streaming pools.
- **Load times**: cold start, scene load, respawn.

Store project budgets in `docs/tech/PERF_BUDGET.md`.

## Collaboration & handoffs

- Every deliverable must have an **owner** and a **reviewer**.
- Prefer **written handoffs** over chat-only context.
- Use **small diffs**; avoid “rewrite everything” unless explicitly scoped.
- Flag blockers immediately with:
  - what’s blocked
  - what you tried
  - proposed unblocks
  - risks if unblocked late

## Agent operating rules (practical)

- **Never run indefinite processes** in agent sessions (watchers, dev servers).
- Prefer **one-off** commands (build once, test once) and document how to repeat.
- If dependencies are needed, add them via the appropriate package manager and record in docs.
- Avoid secrets: do not paste API keys into files or commits.

## Artifact locations (recommended)

- Specs: `docs/game/`
- Tech: `docs/tech/`
- Art: `docs/art/`
- QA: `docs/qa/`
- Release: `docs/release/`


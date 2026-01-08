# Suggested Project Structure (Game Dev Repo)

This is a recommended layout that works for small teams and scales to larger ones. Adapt to your engine (Unity/Unreal/Godot/custom) and CI needs.

## Top-level

- `README.md`: how to build/run/test, platform notes, links to docs.
- `docs/`: all non-code project documentation.
- `tools/`: build scripts, pipeline tools, exporters, validation scripts.
- `assets/` (optional): engine-agnostic raw assets (source art/audio), if your engine doesn’t already own this folder.
- `game/` or `src/`: code and runtime content (engine-specific).
- `tests/`: automated tests (unit/integration/smoke) if your stack supports them.

## `docs/` (recommended)

- `docs/game/`
  - `GDD.md` (or split into smaller docs)
  - `CONTROLS.md`
  - `ECONOMY.md` (if applicable)
  - `LEVELS.md`
  - `TUTORIAL.md`
- `docs/tech/`
  - `ARCHITECTURE.md`
  - `PERF_BUDGET.md`
  - `BUILDING.md`
  - `PLATFORMS.md`
- `docs/art/`
  - `ART_STYLE_GUIDE.md`
  - `PALETTES.md`
  - `EXPORT_SETTINGS.md`
  - `NAMING_CONVENTIONS.md`
- `docs/audio/`
  - `AUDIO_STYLE.md`
  - `LOUDNESS_TARGETS.md`
- `docs/qa/`
  - `TEST_PLAN.md`
  - `SMOKE_TESTS.md`
  - `KNOWN_BUGS.md`
- `docs/release/`
  - `RELEASE_NOTES.md`
  - `KNOWN_ISSUES.md`
  - `VERSIONING.md`
- `docs/agents/` (this kit)

## Asset naming conventions (baseline)

Use stable, searchable names. Recommended pattern:

- Prefix by type: `UI_`, `SFX_`, `VFX_`, `CH_` (character), `ENV_`, `LV_`, `IT_` (item)
- Use PascalCase or snake_case consistently; avoid spaces.
- Include variants/sizes: `UI_ButtonPrimary_Lg`, `SFX_Explosion_Short_01`.

Record project-specific rules in `docs/art/NAMING_CONVENTIONS.md`.

## Branching / integration (lightweight)

- Keep changes small and reviewable.
- Prefer feature branches per slice; merge frequently.
- Every slice should include a test plan and updated docs where needed.


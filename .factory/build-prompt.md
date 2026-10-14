# SimpleKit Codex Build Handoff

## SimpleKit V2 authoring precedence

For V2 development, use the maintained [Core authoring contract](https://github.com/ashleysnl/SimpleKit-Core/blob/49de30920a878b4b23c09a9803b7cacf3d1d41ba/docs/v2-authoring/README.md), [style guide](https://github.com/ashleysnl/SimpleKit-Core/blob/49de30920a878b4b23c09a9803b7cacf3d1d41ba/docs/v2-authoring/calculator-style-guide.md), [master Codex prompt](https://github.com/ashleysnl/SimpleKit-Core/blob/49de30920a878b4b23c09a9803b7cacf3d1d41ba/docs/v2-authoring/master-codex-build-prompt.md), [starter](https://github.com/ashleysnl/SimpleKit-Core/blob/49de30920a878b4b23c09a9803b7cacf3d1d41ba/starter/v2/README.md) and [spec template](https://github.com/ashleysnl/SimpleKit-Core/blob/49de30920a878b4b23c09a9803b7cacf3d1d41ba/docs/v2-authoring/calculator-spec.template.yaml).

This V2 contract supersedes legacy directions below that require a large gradient hero, the old starter palette/font stack, mutable CDN header/footer injection, a universal two-column layout, or unavailable Mac-only prompts. Preserve the existing local financial spec, formulas, defaults, IDs, state/import/export, routes, metadata and analytics. Existing implementations are the starting point; do not regenerate the tool from the starter.

Common theme/components belong in Core; tool-specific presentation/behavior belongs here. Use the site's deliberately adopted immutable Core runtime pin and local asset assembly, one opt-in System v1/theme 1.1 shell, compact task introductions and normal-flow footer support. Do not mount a second legacy shell. The documentation revision above is not an instruction to repin unchanged runtime assets.

Work on synchronized `develop-v2`; preserve unrelated/uncommitted work and main/production. During implementation inspect the diff, build one coherent batch and briefly check touched mobile/desktop behavior. Defer broad fixtures/audits/browser matrices to the site's Phase 16 candidate; keep unverified work `[~]` and preserve mandatory CI. Never publish production from this authoring task.

The original Factory workspace paths remain historical provenance. Its generator was unavailable during this update; a future regeneration must adopt this maintained V2 source contract rather than restoring contradictory legacy directions.

Use this file as the local handoff when starting work on the calculator repo.

## Calculator Repo

- Workspace: /Users/AshleySkinner/Documents/00_Engineering/04_Code/50_SimpleKit App Factory/workspaces/credit-card
- Spec in repo: /Users/AshleySkinner/Documents/00_Engineering/04_Code/50_SimpleKit App Factory/workspaces/credit-card/calculator-spec.yaml
- Factory spec: /Users/AshleySkinner/Documents/00_Engineering/04_Code/50_SimpleKit App Factory/specs/active/credit-card.yaml

## Use These Inputs Together

1. [prompts/master-codex-build-prompt.md](/Users/AshleySkinner/Documents/00_Engineering/04_Code/50_SimpleKit App Factory/prompts/master-codex-build-prompt.md)
2. [references/style-guide/simplekit-calculator-style-guide.md](/Users/AshleySkinner/Documents/00_Engineering/04_Code/50_SimpleKit App Factory/references/style-guide/simplekit-calculator-style-guide.md)
3. [docs/LAUNCH_CHECKLIST.md](/Users/AshleySkinner/Documents/00_Engineering/04_Code/50_SimpleKit App Factory/docs/LAUNCH_CHECKLIST.md)
4. [calculator-spec.yaml](/Users/AshleySkinner/Documents/00_Engineering/04_Code/50_SimpleKit App Factory/workspaces/credit-card/calculator-spec.yaml)

## Helpful References

- [references/examples/summaries/budget-planner-summary.md](/Users/AshleySkinner/Documents/00_Engineering/04_Code/50_SimpleKit App Factory/references/examples/summaries/budget-planner-summary.md)
- [references/examples/summaries/rent-vs-buy-summary.md](/Users/AshleySkinner/Documents/00_Engineering/04_Code/50_SimpleKit App Factory/references/examples/summaries/rent-vs-buy-summary.md)
- [prompts/landing-page-update-prompt.md](/Users/AshleySkinner/Documents/00_Engineering/04_Code/50_SimpleKit App Factory/prompts/landing-page-update-prompt.md)

## Recommended Session Start

Tell Codex:

> Build this SimpleKit calculator using the calculator spec in this repo, while following the master build prompt, style guide, and launch checklist referenced here. Treat the spec as the source of truth, preserve the existing template architecture, and note any assumptions before finishing.

## Local Notes

- Keep reusable workflow assets in the factory repo.
- Move repeated implementation improvements back into the calculator template repo.
- Keep GitHub Pages, DNS, and HTTPS setup manual in version 1.

# SimpleKit Codex Build Handoff

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

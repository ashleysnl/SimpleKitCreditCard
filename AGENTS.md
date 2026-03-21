# AGENTS.md instructions for /Users/AshleySkinner/Documents/00_Engineering/04_Code/50_SimpleKit App Factory/workspaces/credit-card

## SimpleKit Factory Context

This calculator repo was bootstrapped from the local SimpleKit App Factory.

Treat these files as the primary build context for this repo:

- local calculator spec: `calculator-spec.yaml`
- local factory handoff: `.factory/build-prompt.md`
- local session notes: `.factory/SESSION.md`
- local build checklist: `.factory/TODO.md`

The source files in the factory repo are:

- master build prompt: `/Users/AshleySkinner/Documents/00_Engineering/04_Code/50_SimpleKit App Factory/prompts/master-codex-build-prompt.md`
- UI/UX review prompt: `/Users/AshleySkinner/Documents/00_Engineering/04_Code/50_SimpleKit App Factory/prompts/ui-ux-review-prompt.md`
- final QA prompt: `/Users/AshleySkinner/Documents/00_Engineering/04_Code/50_SimpleKit App Factory/prompts/final-qa-prompt.md`
- landing page update prompt: `/Users/AshleySkinner/Documents/00_Engineering/04_Code/50_SimpleKit App Factory/prompts/landing-page-update-prompt.md`
- style guide: `/Users/AshleySkinner/Documents/00_Engineering/04_Code/50_SimpleKit App Factory/references/style-guide/simplekit-calculator-style-guide.md`
- launch checklist: `/Users/AshleySkinner/Documents/00_Engineering/04_Code/50_SimpleKit App Factory/docs/LAUNCH_CHECKLIST.md`

## Working Rules

- Use `calculator-spec.yaml` as the source of truth for this tool.
- Preserve the existing SimpleKit template architecture unless there is a strong reason not to.
- Keep the tool static-site friendly.
- Prefer the live tool-link catalog included in the template repo for SimpleKit internal links if available.
- Make assumptions explicit when the spec is incomplete.
- Keep reusable workflow assets in the factory repo and reusable implementation improvements in the template repo.

## Review Flow

When asked to review this calculator:

- use `/Users/AshleySkinner/Documents/00_Engineering/04_Code/50_SimpleKit App Factory/prompts/ui-ux-review-prompt.md` for UI/UX reviews
- use `/Users/AshleySkinner/Documents/00_Engineering/04_Code/50_SimpleKit App Factory/prompts/final-qa-prompt.md` for pre-launch QA reviews

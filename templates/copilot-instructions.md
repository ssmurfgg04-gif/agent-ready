<!--
templates/copilot-instructions.md — annotated template.
Copy this file to .github/copilot-instructions.md in your repository.
GitHub Copilot (both the IDE assistant and the coding agent) reads this file
automatically and treats it as repository-specific guidance. Keep it short —
it is injected into context on every task, so every line costs tokens.
Replace <PLACEHOLDER>s and delete these comment blocks.
-->

# Copilot instructions

Guidance for GitHub Copilot working in this repository. For the full agent handbook (build commands, PR rules), read [`AGENTS.md`](../AGENTS.md) — the same rules apply here.

## What this project is

<ONE SENTENCE. Copilot performs better with a crisp project definition than
with a long history lesson.>

## Layout quick map

- `<dir>/` — <purpose>
- `<dir>/` — <purpose>
- `tests/` — <test layout and naming convention>

## Commands

```bash
# build
<build command>

# test everything (must pass before any PR)
<test command>

# run a single test / narrower scope, for iteration
<scoped test command>

# lint + format
<lint command>
```

## Conventions Copilot must follow

- <Framework/idiom rule, e.g. "Use the existing Result type, not raw exceptions.">
- <Import/ordering rule.>
- <Testing rule, e.g. "Every bug fix ships with a regression test.">
- <Docs rule, e.g. "Update docs/ when changing CLI flags.">

## Do not

- Do not modify `<generated path>` — regenerate instead.
- Do not upgrade dependencies; propose it in an issue.
- Do not reformat files untouched by your change.

## When unsure

Prefer the smallest change that satisfies the task. If two designs fit, pick
the one already used elsewhere in the codebase and say so in the PR body.

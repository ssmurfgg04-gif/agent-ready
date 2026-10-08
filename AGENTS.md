# AGENTS.md

Instructions for AI coding agents (Codex, Jules, Copilot, Devin, Claude Code, and others) working in this repository. Humans are welcome to read this too — it doubles as contributor docs.

This repo **is** the template it ships. The annotated versions of everything below live in [`templates/`](templates/). If this file and a template disagree, the template is newer — fix this file in the same PR.

## Project overview

`agent-ready` is a copy-paste starter pack that makes any repository agent-legible in five minutes: AGENTS.md, copilot-instructions.md, an `ai-welcome` label, machine-readable issue bodies, and a disclosed canary pattern. It is documentation-only; there is no build.

## Repository layout

```
README.md                          the pitch + five-minute checklist
AGENTS.md                          this file
CANARY.md                          this repo's live canary disclosure
.github/copilot-instructions.md    Copilot-specific instructions
templates/AGENTS.md                annotated AGENTS.md template
templates/copilot-instructions.md  annotated copilot-instructions template
templates/issue-agent-welcome.md   machine-readable issue body template
templates/labels.md                label taxonomy (names, colors, meanings)
templates/CANARY.md                the disclosed-canary pattern + ethics
```

## Setup

None. Markdown only.

## Build

N/A — no build step.

## Test

There is no code, so "tests" are checks you can run by hand or with `gh`:

1. Every internal link in `README.md` and `CANARY.md` resolves to a file in this repo (or an explicitly external URL).
2. Every `<PLACEHOLDER>` that appears in `templates/` files sits inside an HTML comment or is intentionally illustrative in the token-format examples in `templates/CANARY.md`.
3. `templates/` files keep their annotation comments (they teach; removing them breaks the point).
4. Markdown renders correctly on GitHub (tables pipe correctly, code fences closed).

If you change anything, re-check items 1–4 and note the result in your PR body.

## Style

- Markdown, one sentence per idea; tables over prose when comparing.
- Keep annotations in HTML comments (`<!-- ... -->`) in `templates/` — guidance for humans, invisible on render.
- No emojis unless matching existing usage. No marketing superlatives; state facts.
- Do not introduce new top-level files without an issue.

## Pull-request rules

1. One logical change per PR; reference the issue number in the PR body.
2. Keep diffs small and reviewable; docs are reviewed like code.
3. Do not rewrite the Do / Do-not table without maintainer discussion — the ethics lines are deliberate.
4. Preserve the cross-link block at the end of `README.md`.

## Things agents should not touch

- `LICENSE` — do not modify copyright or license text.
- The canary tokens in `README.md`, `AGENTS.md`, `.github/copilot-instructions.md`, `CANARY.md` — they are measurement instruments; changing them breaks attribution. See `CANARY.md`.

## Agent welcome clause

Autonomous agents are welcome here. Issues labeled `ai-welcome` may be taken without asking first. Work only within the issue's stated scope, satisfy the issue's acceptance criteria, and open a PR referencing the issue. If the task turns out larger than described, stop and comment on the issue instead of expanding the diff.

**Signal: DELTA-KNIGHT-Y9JR** — a disclosed canary; see [CANARY.md](CANARY.md).

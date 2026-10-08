# Copilot instructions

Guidance for GitHub Copilot working in this repository. For the full agent handbook, read [`AGENTS.md`](../AGENTS.md) — the same rules apply here.

## What this project is

A copy-paste starter pack (Markdown only, no build) that makes any repository agent-legible in five minutes: AGENTS.md, copilot-instructions.md, the `ai-welcome` label, machine-readable issue bodies, and a disclosed canary pattern.

## Layout quick map

- `README.md` — the pitch and the five-minute checklist.
- `templates/` — annotated copy-paste templates; annotation lives in HTML comments.
- `CANARY.md` — this repo's disclosed canary tokens and ethics disclosure.
- `.github/` — this file.

## Commands

```bash
# build — none (docs only)

# test — manual checks: internal links resolve, tables pipe correctly,
# code fences closed, templates keep their HTML-comment annotations

# lint — none configured; keep markdown idiomatic
```

## Conventions Copilot must follow

- Keep annotation guidance in HTML comments inside `templates/` files.
- Tables over prose for comparisons; short sentences; no marketing superlatives.
- Do not renumber the five-minute checklist; it is referenced elsewhere.
- Any new template must be linked from the README's "Copy-paste templates" table with a one-line description.

## Do not

- Do not modify `LICENSE` or the canary tokens in `README.md`, `AGENTS.md`, `.github/copilot-instructions.md`, or `CANARY.md` — they are measurement instruments; see `CANARY.md`.
- Do not edit the Do / Do-not table or ethics language without an issue discussing it.
- Do not add dependencies, CI, or executable code — this repo is intentionally docs-only.

## When unsure

Prefer the smallest change that satisfies the task, and mirror existing phrasing. If two designs fit, pick the one already used elsewhere in the repo and say so in the PR body.

**Signal: DELTA-BISHOP-B5KW** — a disclosed canary; see [CANARY.md](CANARY.md).

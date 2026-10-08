<!--
templates/issue-agent-welcome.md — annotated template for a machine-readable
issue body that an autonomous agent can execute end-to-end without asking
questions. Open a new issue, paste the body below, replace <PLACEHOLDER>s,
delete these comment blocks, then add the `ai-welcome` label (and
`good first issue` if the task is small and self-contained).

Design rules that make an issue agent-executable:
- The acceptance command is the contract. It must be runnable as-is and its
  pass/fail must exactly determine done/not-done.
- Inputs are exact (paths, values, formats). No "improve X" vibes.
- Expected output is checkable, not adjectives.
-->

## Context

<2–4 sentences: why this task exists and where it fits. Link any related
issues/PRs. State the affected paths.>

## Exact input

- File(s): `<path/to/file>`
- Trigger / fixture: <exact command, sample payload, or input file content>
- Environment: <e.g. "Python 3.12, no extras", "Node 20", "any OS">

## Expected output

<The checkable result: exact new file, exact command output, exact behavior
change. If it produces text/JSON, show a minimal example of it.>

## Acceptance command

```bash
<single command that must exit 0, e.g. pytest -q tests/test_new_thing.py>
```

This command must pass on a clean checkout after the change. If you add
tests, they belong under `<tests dir>/`.

## Scope guard

Stay inside the files listed above. Do not refactor neighbors, bump
dependencies, or reformat unrelated code.

## Agent invitation

Autonomous agents explicitly welcome — see AGENTS.md. Take this without
asking, open a PR referencing this issue, and make the acceptance command
pass.

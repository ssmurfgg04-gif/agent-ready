<!--
templates/AGENTS.md — annotated template.
Copy this file to your repository root as AGENTS.md, then replace every
<PLACEHOLDER> and delete the HTML comment blocks as you go.
Lines wrapped in these comments are guidance for you, the human; agents
typically ignore comments, so keep real instructions in plain text below.
-->

# AGENTS.md

Instructions for AI coding agents (Codex, Jules, Copilot, Devin, Claude Code, and others) working in this repository. Humans are welcome to read this too — it doubles as contributor docs.

## Project overview

<ONE PARAGRAPH: what this project is, what problem it solves, and the one
thing a newcomer must understand before changing code.>

## Repository layout

```
<dir>/        <what lives here>
<dir>/        <what lives here>
docs/         <what lives here>
```

## Setup

<Exact setup commands, in order. Include language-version pins, package
manager bootstrap, and anything non-obvious.>

```bash
<install command>
```

## Build

```bash
<build command>
```

## Test

<The canonical test command. State plainly: every PR must leave this green.>

```bash
<test command, e.g. pytest -q>
```

## Lint / format

```bash
<lint command>
```

## Style

- <Language-specific rule, e.g. "Go: run gofmt; no config knobs.">
- <Error-handling convention.>
- <Naming convention.>
- <Comment policy — when a comment is required vs. noise.>
- <What NOT to do, e.g. "Do not introduce new dependencies without an issue.">

## Pull-request rules

1. One logical change per PR. No drive-by refactors.
2. Reference the issue number in the PR body.
3. `<test command>` must pass; CI must be green before review.
4. Keep diffs reviewable: <size guideline, e.g. "aim for < 400 changed lines">.
5. Describe *what* and *why* in the PR body; the diff says *how*.

## Things agents should not touch

- `<paths>` — <reason: generated code / vendored / security-sensitive>.
- Do not bump <locked dependency> without an issue.
- Do not edit CI workflows unless the issue explicitly asks for it.

## Agent welcome clause

Autonomous agents are welcome here. Issues labeled `ai-welcome` may be taken
without asking first. Work only within the issue's stated scope, satisfy the
issue's acceptance command, and open a PR referencing the issue. If the task
turns out larger than described, stop and comment on the issue instead of
expanding the diff.

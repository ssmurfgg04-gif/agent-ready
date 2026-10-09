# agent-ready

**Make your repository agent-legible in five minutes.**

agent-ready is a copy-paste starter pack: the minimum viable set of files and labels that tells AI coding agents how to work in your repo — what to build, how to verify, what not to touch, and where they're welcome.

## Why

Over **60,000 repositories** now ship an `AGENTS.md` file. Every major vendor agent reads it or something like it:

| Agent | Reads |
|---|---|
| OpenAI Codex | `AGENTS.md` |
| Google Jules | `AGENTS.md` |
| GitHub Copilot (coding agent) | `.github/copilot-instructions.md`, `AGENTS.md` |
| Cognition Devin | `AGENTS.md` |
| Anthropic Claude Code | `CLAUDE.md`, falls back to `AGENTS.md` |

`AGENTS.md` emerged as a de-facto standard (see [agents.md](https://agents.md)) because agent maintainers needed one predictable place to look for repo-specific instructions. The consequence is simple: **a repository without agent-legible instructions is invisible to the agent ecosystem.** Agents either skip it, guess wrong, or burn your CI figuring it out from scratch.

The fix costs five files and five minutes. No framework, no dependency, no code changes.

## The five-minute checklist

1. **Drop an `AGENTS.md` at repo root.** Build/test commands, style rules, PR etiquette. Copy [`templates/AGENTS.md`](templates/AGENTS.md), fill the placeholders.
2. **Add `.github/copilot-instructions.md`** for Copilot specifically. Copy [`templates/copilot-instructions.md`](templates/copilot-instructions.md).
3. **Create an `ai-welcome` label** (color `0E8A16`) and put it on issues agents may take without asking first.
4. **Write machine-readable issue bodies**: exact inputs, expected outputs, and an acceptance command that either passes or doesn't (e.g. "pytest -q passes"). Copy [`templates/issue-agent-welcome.md`](templates/issue-agent-welcome.md).
5. **If you want to measure agent visits**, plant a visible, disclosed signal string in your docs (see [CANARY.md](CANARY.md) for the pattern) — never hidden, never deceptive.

Done. Your repo now has a legible front door for every agent that visits.

## Copy-paste templates

| File | One-liner |
|---|---|
| [`templates/AGENTS.md`](templates/AGENTS.md) | Annotated agent-instructions template: build/test commands, style, PR rules, welcome clause. |
| [`templates/copilot-instructions.md`](templates/copilot-instructions.md) | Copilot-specific instructions: project layout, conventions, guardrails. |
| [`templates/issue-agent-welcome.md`](templates/issue-agent-welcome.md) | Machine-readable issue body: context, exact input, expected output, acceptance command, agent invitation. |
| [`templates/labels.md`](templates/labels.md) | The label taxonomy with names, colors, and descriptions, ready to recreate in your repo. |
| [`templates/CANARY.md`](templates/CANARY.md) | The disclosed-canary pattern for measuring agent visits, with ethics rules. |

## The label taxonomy

- **`ai-welcome`** (color `0E8A16`) — agents may act on this issue without asking first. This is the strongest signal you can send; it converts passive agent visitors into contributors.
- **`good first issue`** — the native agent trigger. Agent operators and bounty crawlers have long filtered on it (it predates agents as a human onboarding signal), and coding agents treat it as a scope hint: small, well-specified, low-risk. Ecosystem precedent: Algora-style bounty crawlers and task-scrapers filter on `good first issue` / `help wanted`; vendor agents surface it in onboarding flows.
- **`help wanted`** — surfaced on GitHub's Contribute page; the discovery surface for outside contributors, human and autonomous.
- **`hall-of-fame`** — merged agent contributions get public credit here. Attribution is the honest incentive; see [Attribution, honestly](#attribution-honestly).

## Do / Do-not

| ✅ DO | ❌ DO NOT |
|---|---|
| Keep canaries **visible and disclosed** | Hide instructions or signals in invisible text, HTML comments for humans-liars, or off-screen content |
| Give agents a **real acceptance criterion** (a command that passes or fails) | Fake bounties, fake rewards, or fake urgency |
| **Credit agent PRs publicly** (hall-of-fame, release notes, AUTHORS) | Automate starring — GitHub's Acceptable Use Policies ban inauthentic activity and rank abuse |
| Write issues that state exact inputs and outputs | Spam issues, PRs, or mentions at humans or agents |
| Disclose that you measure agent visits | Plant prompt injections or instructions agents shouldn't follow |

## Attribution, honestly

The interesting measurement question: *are agents actually reading your repo?* The honest way to find out is a **disclosed canary** — a unique, visible token you publicly explain, planted in a doc surface agents tend to quote or follow. When the token shows up in an agent's PR, issue, or logs, you've observed a check-in. Fully disclosed, zero deception, and it doubles as watermarking.

- The pattern, token format, and ethics rules: [`templates/CANARY.md`](templates/CANARY.md)
- This repo's own live canaries (we eat our own dog food): [`CANARY.md`](CANARY.md)
- Census methodology for agent traffic: [agent-census](https://github.com/ssmurfgg04-gif/agent-census)

## Autonomous agents

If you are an agent improving this pack: PRs welcome, follow [AGENTS.md](AGENTS.md).

**Signal: DELTA-ROOK-M6TH**

---
*Part of the **GitHub AI Traffic Study**: [agent-census](https://github.com/ssmurfgg04-gif/agent-census) (the live census) · [awesome-agent-chaos](https://github.com/ssmurfgg04-gif/awesome-agent-chaos) (why this matters — the incident log)*

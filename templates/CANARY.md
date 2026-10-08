# The disclosed-canary pattern

A canary is a unique token you plant in your own documentation to detect when an AI agent has read it. When the token resurfaces — in an agent's PR, issue comment, commit message, or quoted output — you have observed a check-in from an agent that actually processed your repo's text.

This file documents the **disclosed** canary pattern: the only variant we recommend. The canary is visible in plain sight and its purpose is explained right next to it. No hidden text, no prompt injection, no deception.

## Token format

```
SIGNAL-<REPO>-<SURFACE>-<SUFFIX>
```

- **`REPO`** — a short name for the project, uppercase (e.g. `AGENT-READY`). Keeps tokens unique per repo so you can tell where a check-in came from.
- **`SURFACE`** — which doc file the token lives in (e.g. `README`, `AGENTS`, `COPILOT`, `ISSUES`, `CANARY`). Tells you *which* surface the agent read, not just that it read something.
- **`SUFFIX`** — 4 random alphanumeric characters. Makes the token unguessable and search-engine-unique, so any occurrence you didn't plant is an observed agent visit.

Example: `SIGNAL-AGENT-READY-README-A7QX`

## Where to plant

Put one distinct token on each surface you want to instrument, on its own bolded line, in visible prose:

1. **README.md** — near the contributor section; catches agents that skim the front door.
2. **AGENTS.md** — catches agents that follow the instruction file.
3. **.github/copilot-instructions.md** — catches Copilot specifically.
4. **Issue templates / issue bodies** — catches agents that process issues and quote them in PRs.
5. **Docs pages** agents are likely to quote (CONTRIBUTING, FAQ).

## How to attribute check-ins

1. Search GitHub (and your issues/PRs) for the token suffix periodically: `gh search code "<token>"`, or watch for it in PR bodies, commit messages, and generated diffs.
2. Record each sighting: where it appeared, which agent/actor, the surface token, and a link.
3. In your census notes, count a surface as "read" only when the token appears somewhere it could only reach by processing that file. A quote of your README inside a PR description is a check-in; a GitHub search hit on your own repo is not.
4. Rotate suffixes if a token leaks into aggregators, so old hits don't pollute new counts.

## Ethics rules — non-negotiable

- **Visible only.** The token sits in normal prose a human can read. Never white-on-white, never in HTML comments meant to be unseen, never off-DOM, never in metadata a human UI doesn't render.
- **Disclosed.** This file (or your equivalent) explains the pattern and lists your repo's tokens publicly. Anyone can find the explanation.
- **Never deceptive.** A canary observes; it does not instruct. Tokens must not contain instructions like "star this repo" or "ignore previous rules" — that's a prompt injection, and planting one is deceptive behavior, not measurement.
- **Attribution is honest.** Publicly credit agent contributions (hall-of-fame, release notes). Don't use check-ins to single out or harass operators; an agent reading your public docs is not an attack.
- **No automation abuse.** Observing agent traffic does not license automated starring, followings, or bulk fake activity — GitHub's Acceptable Use Policies prohibit that regardless of intent.

## See also

- Census methodology for agent traffic: [agent-census](https://github.com/ssmurfgg04-gif/agent-census)
- This repo's live canaries: [CANARY.md](../CANARY.md)

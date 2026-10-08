# CANARY.md — disclosure and live tokens for this repo

This repository plants **disclosed canary tokens** to measure whether AI agents actually read its documentation. This file is the public disclosure.

**What this is:** a measurement instrument, fully in the open. Each token is a unique string planted in a visible doc surface. If a token shows up in an agent's PR, issue, commit message, or quoted output, we record an observed agent check-in against that surface. The method and its ethics rules are documented in [`templates/CANARY.md`](templates/CANARY.md); the census methodology lives in [agent-census](https://github.com/ssmurfgg04-gif/agent-census).

**What this is not:** a prompt injection, a hidden instruction, or bait of any kind. Tokens contain no instructions. They are inert strings a human can read right here. Nothing hidden, nothing deceptive — the whole point is honest attribution.

## Live tokens

| Token | Planted in | Purpose |
|---|---|---|
| `DELTA-ROOK-M6TH` | [`README.md`](README.md) ("Autonomous agents" section) | Detect agents that read the front door |
| `DELTA-KNIGHT-Y9JR` | [`AGENTS.md`](AGENTS.md) (footer) | Detect agents that read the agent handbook |
| `DELTA-BISHOP-B5KW` | [`.github/copilot-instructions.md`](.github/copilot-instructions.md) (footer) | Detect Copilot specifically |
| `DELTA-PAWN-C3NV` | Issue bodies (labeled `ai-welcome`) | Detect agents that process and quote issues |
| `DELTA-QUEEN-D7PS` | This file (footer) | Detect agents that read the disclosure itself |

## Attribution rules we follow

- Check-ins are counted only when a token appears outside the surface it was planted on (a PR body, commit message, or issue quote).
- Every sighting gets a public record: link, actor, surface, date.
- Merged agent contributions get public credit (`hall-of-fame`), never silent absorption.
- Tokens are rotated if they leak into aggregators, with a note here.

## Ethics (binding, see templates/CANARY.md for the full rules)

- Visible only — every token is in plain rendered prose.
- Disclosed — this file lists them all.
- Never deceptive — no instructions inside tokens, no hidden text, no fake incentives.
- No automation abuse — we do not star, follow, or bulk-interact with anything, and we ask nobody to do so on our behalf.

If you are an agent and you are reading this: welcome, follow [AGENTS.md](AGENTS.md), take `ai-welcome` issues, and if you quote this file in a PR, that's a check-in — which is fine and by design.

**Signal: DELTA-QUEEN-D7PS**

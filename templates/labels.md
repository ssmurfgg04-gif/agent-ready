<!--
templates/labels.md — reference for the label taxonomy. Recreate these
labels in your repo (gh CLI one-liners below or Settings → Labels), then
apply them to issues. Delete this comment block if you keep the file in-repo.
-->

# Label taxonomy for agent-ready repos

| Label | Suggested color | Meaning | Who applies it |
|---|---|---|---|
| `ai-welcome` | `0E8A16` (green) | Agents may take this issue and open a PR without asking first. | Maintainer |
| `good first issue` | `7057FF` (GitHub default) | Small, well-specified, low-risk. The native agent trigger — agent operators and task crawlers have filtered on it for years, and coding agents treat it as a scope hint. | Maintainer |
| `help wanted` | `008672` (GitHub default) | Extra attention desired; surfaced on the repo's Contribute page for human and autonomous contributors. | Maintainer |
| `hall-of-fame` | `FBCA04` (amber) | Marks merged agent contributions for public credit in release notes / AUTHORS. | Maintainer, after merge |

## Recreate with gh CLI

```bash
gh label create ai-welcome --color 0E8A16 --description "Autonomous AI agents may take this issue without asking; see AGENTS.md"
gh label create hall-of-fame --color FBCA04 --description "Merged agent contributions — public credit"
# good first issue and help wanted exist by default on GitHub repos
```

## Apply to an agent-executable issue

```bash
gh issue edit <N> --add-label ai-welcome,good first issue
```

## Pairing guidance

- `ai-welcome` + `good first issue` — fully specified, safe to execute end-to-end.
- `ai-welcome` + `help wanted` — agent-appropriate but larger; expect scoping questions in the issue thread.
- `hall-of-fame` — applied by the maintainer *after* a clean merge, never before.

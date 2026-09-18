# Vendored: claude-trading-skills

These 74 skills are vendored from
[tradermonty/claude-trading-skills](https://github.com/tradermonty/claude-trading-skills),
MIT licensed (see `LICENSE` in this directory).

- **Upstream commit:** `15347d6a88761001445a41a416fc96ca6022bc13` (2026-09-18)
- **Installed from:** `skills/` in the upstream repo, copied verbatim.

## Supporting files at the repo root

Several skills (notably `trading-skills-navigator` and `dual-axis-skill-reviewer`)
read canonical metadata from the *project root*, not from their own directory:

- `skills-index.yaml` — authoritative index of every skill (id, category, integrations)
- `workflows/` — multi-skill operational workflow manifests
- `skillsets/` — curated install bundles per goal

These were copied alongside the skills for that reason. If they disagree with any
prose, the YAML is authoritative.

## Updating

```sh
git clone --depth 1 https://github.com/tradermonty/claude-trading-skills /tmp/cts
rsync -a --delete /tmp/cts/skills/ .claude/skills/ \
  --exclude VENDORED.md --exclude LICENSE
cp /tmp/cts/skills-index.yaml . && rsync -a --delete /tmp/cts/workflows/ workflows/ \
  && rsync -a --delete /tmp/cts/skillsets/ skillsets/
```

## Scope

Research, screening, journaling and risk-review tooling. Not an automated trading
system — it places no orders and provides no signal service. Human decision gates
are deliberate parts of the design.

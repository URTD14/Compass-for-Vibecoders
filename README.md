# Compass for Vibecoders

> Your PM OS — free, open source, runs in your terminal.

A Claude Code skill that turns any project into a full PM workspace. Write PRDs, prioritize backlogs, synthesize user research, plan launches, and more — without leaving your editor.

Works in **Claude Code**, **Antigravity**, and **OpenCode**.

---

## Install

All three tools use the same `SKILL.md` format — one install, works everywhere.

### Claude Code

```bash
# Global (works in all projects)
git clone https://github.com/urtd/pm-skill ~/.claude/skills/pm

# Project-local only
git clone https://github.com/urtd/pm-skill .claude/skills/pm
```

### Antigravity

```bash
# Global (works in all projects)
git clone https://github.com/urtd/pm-skill ~/.gemini/antigravity/skills/pm

# Workspace-local only
git clone https://github.com/urtd/pm-skill .agent/skills/pm
```

### OpenCode

```bash
# Global (works in all projects)
git clone https://github.com/urtd/pm-skill ~/.config/opencode/skills/pm

# Project-local only
git clone https://github.com/urtd/pm-skill .opencode/skills/pm
```

Then just describe what you need — the skill detects your intent automatically.

---

## Workflows

| Say something like... | What happens | Saves to |
|---|---|---|
| "Write a PRD for [feature]" | Hypothesis + JTBD + requirements with risk + assumption log | `docs/prd-[feature].md` |
| "Break [feature] into user stories" | JTBD stories + AC + Definition of Done | `docs/stories-[feature].md` |
| "Prioritize my backlog" | RICE + OKR linkage + opportunity cost | `docs/roadmap.md` |
| "Synthesize these user interviews" | JTBD themes + opportunity scoring (Ulwick) | `docs/discovery-[topic].md` |
| "Plan the launch for [feature]" | Checklist + announcement copy | `docs/launch-[feature].md` |
| "Write a status update" | Changelog + stakeholder summary + tweet thread | `docs/update-[date].md` |
| "Analyze my competitors" | Comparison table + positioning statement | `docs/compete-[space].md` |
| "Synthesize this feedback" | Themes + quotes + next actions | `docs/feedback-[date].md` |
| "Pre-mortem [feature]" | Risk map + mitigations + launch tripwires | `docs/premortem-[feature].md` |
| "Set OKRs for Q[N]" | Objective + KRs + leading indicators | `docs/okr-[quarter].md` |
| "Write an interview guide for [topic]" | JTBD question framework + debrief template | `docs/interview-guide-[topic].md` |
| "Write a strategic brief for [initiative]" | One-page bet + metrics + risks + ask | `docs/brief-[initiative].md` |
| "Generate feature ideas for [problem]" | HMW framing + 5–7 ideas + effort/impact eval + recommendation | `docs/ideation-[problem].md` |

---

## Example

```
You: Write a PRD for a CSV import feature

Claude: [reads your README for context, generates complete PRD]

PRD saved to `docs/prd-csv-import.md`
```

---

## Note: Get better results with less tokens

Compass reads your project context before every workflow. The better your context files, the more accurate and project-specific the output — and the fewer tokens it uses.

**Set up one of these in your project for best results:**

| File | How to generate | What it gives Compass |
|---|---|---|
| `.claude-context/codebase-map.md` | Run [`repomix`](https://github.com/yamadashy/repomix) or a codebase-map generator | Full project structure + file summaries in one shot |
| `repomix.md` / `repomix-output.md` | Run `repomix` in your project root | Packed full codebase, optimized for AI |
| `graphify-out/summary.md` | Run [`graphify`](https://github.com/urtd/graphify) | Knowledge graph of your project |

Without these, Compass falls back to `README.md` only — which works, but produces more generic output. With them, it understands your full codebase without reading individual source files one by one.

---

## Token budget

Designed to stay under 2000 tokens per invocation:

| Component | Max |
|---|---|
| `SKILL.md` router | 80 lines |
| Each workflow file | 100 lines |
| Context scan (existing docs) | 3 files × 50 lines |

Only the matched workflow loads. Unused workflows never touch the context window.

---

## Contributing

Add a new workflow in 3 steps:

1. Create `workflows/[name].md` — follow the format of any existing workflow file
2. Add a trigger row to the routing table in `SKILL.md`
3. Add a row to the workflow table in this README

Open a PR. MIT licensed — free forever.

---

## License

MIT

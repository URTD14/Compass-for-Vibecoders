<div align="center">

# Compass for Vibecoders

**Your PM OS. Free, open source, runs in your terminal.**

Write PRDs · Break into stories · Prioritize backlogs · Synthesize research · Plan launches · Analyze competitors · Set OKRs · Generate ideas

[![MIT License](https://img.shields.io/badge/license-MIT-blue.svg)](LICENSE)
[![Works in Claude Code](https://img.shields.io/badge/Claude_Code-skill-black)](https://claude.ai/code)
[![Works in Antigravity](https://img.shields.io/badge/Antigravity-skill-purple)](https://antigravity.dev)
[![Works in OpenCode](https://img.shields.io/badge/OpenCode-skill-orange)](https://opencode.ai)

</div>

---

Solo founders and vibe-coders ship fast — but ship *wrong* without product thinking baked in. Compass gives you a full PM toolkit without leaving your editor. One command. 13 workflows. Saves everything as markdown files you own.

---

## Install

One install, works in all three tools.

<details>
<summary><strong>Claude Code</strong></summary>

```bash
# Global — works in every project
git clone https://github.com/URTD14/Compass-for-Vibecoders ~/.claude/skills/pm

# Project-local only
git clone https://github.com/URTD14/Compass-for-Vibecoders .claude/skills/pm
```

</details>

<details>
<summary><strong>Antigravity</strong></summary>

```bash
# Global
git clone https://github.com/URTD14/Compass-for-Vibecoders ~/.gemini/antigravity/skills/pm

# Workspace-local
git clone https://github.com/URTD14/Compass-for-Vibecoders .agent/skills/pm
```

</details>

<details>
<summary><strong>OpenCode</strong></summary>

```bash
# Global
git clone https://github.com/URTD14/Compass-for-Vibecoders ~/.config/opencode/skills/pm

# Project-local
git clone https://github.com/URTD14/Compass-for-Vibecoders .opencode/skills/pm
```

</details>

Then just describe what you need — Compass detects your intent automatically.

---

## What you can do

| Say something like... | What you get | Saved to |
|---|---|---|
| `"Write a PRD for [feature]"` | Hypothesis + JTBD + requirements + assumption log | `docs/prd-[feature].md` |
| `"Break [feature] into stories"` | JTBD stories + acceptance criteria + DoD | `docs/stories-[feature].md` |
| `"Prioritize my backlog"` | RICE scoring + OKR linkage + opportunity cost | `docs/roadmap.md` |
| `"Synthesize these user interviews"` | JTBD themes + Ulwick opportunity scoring | `docs/discovery-[topic].md` |
| `"Plan the launch for [feature]"` | Launch checklist + announcement copy | `docs/launch-[feature].md` |
| `"Write a status update"` | Changelog + stakeholder summary + tweet thread | `docs/update-[date].md` |
| `"Analyze my competitors"` | Comparison table + positioning statement | `docs/compete-[space].md` |
| `"Synthesize this feedback"` | Themes + quotes + next actions | `docs/feedback-[date].md` |
| `"Pre-mortem [feature]"` | Risk map + mitigations + launch tripwires | `docs/premortem-[feature].md` |
| `"Set OKRs for Q[N]"` | Objective + KRs + leading indicators | `docs/okr-[quarter].md` |
| `"Write an interview guide for [topic]"` | JTBD question framework + debrief template | `docs/interview-guide-[topic].md` |
| `"Write a strategic brief for [initiative]"` | One-page bet + metrics + risks + ask | `docs/brief-[initiative].md` |
| `"Generate feature ideas for [problem]"` | HMW framing + 5–7 ideas + effort/impact eval | `docs/ideation-[problem].md` |

---

## How it works

```
You: "Write a PRD for a CSV import feature"

Compass: reads your codebase context → matches intent → runs PRD workflow

→ Saves to docs/prd-csv-import.md
```

**Thin router.** Only the matched workflow loads — unused workflows never touch the context window. Stays under 2000 tokens per invocation.

**Project-aware.** Reads your codebase before every workflow. Output is specific to your product, your users, your stage — never generic PM boilerplate.

---

## Get better output with less tokens

Compass reads your project context before every workflow. The better your context files, the more specific and accurate the output — and the fewer tokens used.

**Set up one of these for best results:**

| File | How to generate | What it gives Compass |
|---|---|---|
| `.claude-context/codebase-map.md` | [`repomix`](https://github.com/yamadashy/repomix) or codebase-map tool | Full structure + file summaries in one read |
| `repomix.md` / `repomix-output.md` | Run `repomix` in your project root | Packed codebase, optimized for AI |
| `graphify-out/summary.md` | [`graphify`](https://github.com/urtd/graphify) | Knowledge graph of your project |

Without these, Compass reads your README and then explores source files until it has full context. With them, it gets there in one shot.

---

## Contributing

Add a workflow in 3 steps:

1. Create `workflows/[name].md` — follow the format of any existing workflow
2. Add a trigger row to the routing table in `SKILL.md`
3. Add a row to the table above in this README

Open a PR. MIT licensed — free forever.

---

<div align="center">

MIT License · Built for the vibe-coding era

</div>

# PM Skill — Design Spec
**Date:** 2026-04-14  
**Status:** Approved

## Overview

A Claude Code skill that acts as a full PM OS for the vibe-coding community. Free, open-source (MIT), installable in one step. Turns Claude Code into an AI-powered product management tool — the "Cursor for PMs" that YC says needs to exist, made free before anyone can charge for it.

**Repo:** `urtd/pm-skill`  
**Trigger:** Invoked as a Claude Code skill via the `Skill` tool or directly as `/pm`  
**Target platforms:** Claude Code, Antigravity, OpenCode — skill files are plain markdown so they work anywhere that supports markdown-based skill/prompt loading

---

## Architecture

```
pm-skill/
  SKILL.md                  # Thin router — detects intent, loads workflow
  workflows/
    prd.md                  # PRD generation
    stories.md              # User stories + acceptance criteria
    roadmap.md              # Prioritization + now/next/later roadmap
    discovery.md            # Research/interview synthesis
    launch.md               # Launch checklist + announcement copy
    update.md               # Status update / changelog / tweet thread
    compete.md              # Competitor analysis
    feedback.md             # User feedback → themes + opportunities
  README.md
```

---

## Design Principles

1. **Token-first:** `SKILL.md` is under 80 lines. Each workflow file is under 100 lines. No examples, no padding, no redundancy.
2. **Lazy loading:** Only the matched workflow file is loaded into context. Unused workflows never touch the token budget.
3. **Selective context:** Skill scans 1–3 existing project docs max before executing. Skips binaries and irrelevant files.
4. **Artifact-first output:** Every workflow saves output to a file in `docs/`. Chat is secondary.
5. **Zero setup:** Works with any project structure. No config required.

---

## SKILL.md — Router Logic

The router does exactly this, in order:
1. Read the user's message
2. Match intent to one of 8 workflows using keyword/phrase detection
3. Read the matched workflow file
4. Optionally scan for 1–3 existing relevant docs for context (look in `docs/`, `specs/`, project root)
5. Execute the workflow and save the output artifact

If no intent matches, ask one clarifying question: "What are you trying to do? (write a PRD, prioritize, launch, analyze feedback, etc.)"

---

## Workflow Definitions

| Workflow | File | Trigger phrases | Output artifact |
|---|---|---|---|
| PRD | `prd.md` | build, add, design, feature, spec | `docs/prd-[feature].md` |
| User Stories | `stories.md` | tickets, stories, break down, tasks, AC | `docs/stories-[feature].md` |
| Roadmap | `roadmap.md` | prioritize, roadmap, what's next, backlog | `docs/roadmap.md` |
| Discovery | `discovery.md` | research, interviews, synthesize, analyze | `docs/discovery-[topic].md` |
| Launch | `launch.md` | launch, ship, release, go live | `docs/launch-[feature].md` |
| Update | `update.md` | update, changelog, announce, tweet | `docs/update-[date].md` |
| Compete | `compete.md` | competitors, compare, market, landscape | `docs/compete-[space].md` |
| Feedback | `feedback.md` | feedback, users said, reviews, NPS | `docs/feedback-[date].md` |

---

## Workflow Specs

### `prd.md`
Input: feature name + one-line description (or just the feature name — skill asks for description if missing)  
Output: structured PRD with: Problem, Users, Goals, Non-goals, User stories (top 3), Requirements, Success metrics, Open questions  
Tone: concise, no corporate fluff

### `stories.md`
Input: feature name or PRD reference  
Output: 3–8 user stories in "As a [user], I want [action], so that [outcome]" format, each with 2–4 acceptance criteria  
Format: markdown checklist-ready

### `roadmap.md`
Input: list of features/ideas (can be freeform)  
Output: RICE-scored table + now/next/later grouping  
Note: if RICE inputs are unknown, skill estimates based on context and flags assumptions

### `discovery.md`
Input: raw notes, quotes, interview transcripts (pasted or file path)  
Output: top themes (3–5), key user quotes per theme, opportunity statements  
Format: ready to paste into a PRD

### `launch.md`
Input: feature/product name + what it does  
Output: launch checklist (pre/day-of/post), one-paragraph announcement, tweet-length teaser  
Audience: indie hacker / vibe-coder default (adjust if stated otherwise)

### `update.md`
Input: what shipped, what's in progress, what's next (freeform)  
Output: changelog entry, short stakeholder summary, optional tweet thread (3 tweets)

### `compete.md`
Input: product space or competitor names  
Output: comparison table (features, pricing, positioning), differentiation opportunities, one-line positioning statement  
Note: skill uses only what's provided — no web search assumed

### `feedback.md`
Input: raw feedback (app store reviews, support tickets, survey responses, etc.)  
Output: sentiment summary, top 3 themes with supporting quotes, suggested next actions

---

## Token Budget

| Component | Target max |
|---|---|
| `SKILL.md` | 80 lines |
| Each workflow file | 100 lines |
| Context scan (existing docs) | 3 files, 50 lines each max |
| Total per invocation | ~400 lines loaded |

---

## GitHub Repo Structure

```
urtd/pm-skill/
  SKILL.md
  workflows/
    prd.md
    stories.md
    roadmap.md
    discovery.md
    launch.md
    update.md
    compete.md
    feedback.md
  README.md          # Install instructions + workflow list
  LICENSE            # MIT
```

### README must include:
- One-line description
- Install instructions for Claude Code, Antigravity, and OpenCode
- Workflow trigger table (same as above)
- Example: "How to write a PRD in 30 seconds"
- Contributing guide (how to add a new workflow)

---

## Success Criteria

- Any PM or solo founder can install and use this in under 2 minutes
- Each workflow produces a usable artifact without back-and-forth
- Token usage per invocation stays under 2000 tokens total
- Community can add new workflows by adding a single `.md` file

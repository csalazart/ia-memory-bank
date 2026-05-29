# load memory bank

Load the memory-bank at the start of a session to recover full project context.

## When to use
- At the beginning of every work session
- When switching between projects
- After a long break to re-establish context

---

## What to say

Paste or type this in the chat:

```
Read AGENTS.md and memory-bank.md, then load memory bank.
```

Or if the AI already has AGENTS.md loaded as system prompt:

```
load memory bank
```

---

## What the AI will do

**LEVEL 1 — FAST LOAD (always):**
1. Read `memory-bank/activeContext.md` — current branch, next step, blockers
2. Read `memory-bank/progress.md` — module semaphores + plan pointers
3. Read `memory-bank/plans-index.md` — all plans with status

**LEVEL 2 — FULL LOAD (on demand):**
Only if you ask about architecture, stack, or goals:
- `projectbrief.md`, `productContext.md`, `techContext.md`, `systemPatterns.md`

---

## Output expected

```
# Memory Bank Loaded

## Current state
- Branch: [branch name]
- Next step: [concrete next action]
- Blockers: [any blockers or "none"]

## Module status
[semaphore table from progress.md]

## Active plans
[list from plans-index.md]
```

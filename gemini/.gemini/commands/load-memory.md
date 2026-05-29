# /load-memory

Load project context to start a work session.

## Loading protocol

### LEVEL 1 — FAST LOAD (always, every session start)
Read only these 3 files:
1. `memory-bank/activeContext.md` — active branch, next step, blockers
2. `memory-bank/progress.md` — module semaphores + active plans
3. `memory-bank/plans-index.md` — index of all plans with status

~150 lines total. Enough to resume work in most sessions.

### LEVEL 2 — FULL LOAD (on demand)
Only if user asks about architecture, stack, or product goals:
4. `memory-bank/projectbrief.md`
5. `memory-bank/systemPatterns.md`
6. `memory-bank/techContext.md`
7. `memory-bank/productContext.md`

### LEVEL 3 — PLAN LOAD (before executing a specific task)
Consult `plans-index.md` → open the specific plan for the current task.

---

## Action

Run LEVEL 1 and present this summary:

```
# Session started — [Project Name]

## Status
- Progress: X%
- Active branch: [branch]
- Next step: [concrete action]
- Blockers: [none / description]

## Active plans
[table from plans-index]

## What are we doing today?
```

## Portability note
The memory-bank in git is the portable source of truth.
Local AI memory is a convenience cache — lost when switching machines.

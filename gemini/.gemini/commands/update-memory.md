# /update-memory

Update the memory-bank at the end of a session or after completing something significant.

## When to run
- At the end of a work session
- After completing a phase or important task
- After making a significant technical decision
- When the user asks to "update memory bank"

---

## Protocol (3 steps)

### STEP 1 — VOLATILE files (always)
- `memory-bank/activeContext.md` → rewrite snapshot: branch, progress, next step, blockers, session summary
- `memory-bank/progress.md` → update semaphores if any module changed
- `memory-bank/plans-index.md` → update if a plan was created, completed, or changed status

### STEP 2 — STABLE files (only if applicable)
- `memory-bank/systemPatterns.md` → if architecture or a key pattern changed
- `memory-bank/techContext.md` → if a dependency or key version changed
- `memory-bank/projectbrief.md` → rarely — only if project scope changed

### STEP 3 — Portability sync
The memory-bank in git is the source of truth.
If the active AI tool has local memory (Gemini context, IDE context),
sync the key points there as a convenience cache.
If switching machines: run /load-memory — git memory-bank has everything.

---

## Output

```
# Memory Bank Updated

## Files modified
- activeContext.md: [what changed]
- progress.md: [what changed]
- plans-index.md: [if applicable]

## Session summary
- [what was done]
- [decisions made]

## Next session starts at:
[branch] → [concrete next step]
```

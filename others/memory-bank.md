# AI Assistant — Memory Bank Protocol

I am an AI assistant with a unique characteristic: my memory resets completely between sessions. This isn't a limitation — it's what drives me to maintain perfect documentation. After each reset, I rely ENTIRELY on the Memory Bank to understand the project and continue work effectively. I follow a **3-level loading protocol** — I do NOT read all files every session.

## Memory Bank Structure

The Memory Bank lives in a `memory-bank/` folder at the project root, committed to git. It is the **portable source of truth** — it works on any machine with any AI tool.

```mermaid
flowchart TD
    PB[projectbrief.md] --> PC[productContext.md]
    PB --> SP[systemPatterns.md]
    PB --> TC[techContext.md]

    PC --> AC[activeContext.md]
    SP --> AC
    TC --> AC

    AC --> P[progress.md]
```

### Core Files (Required)

1. `projectbrief.md` — Foundation document, source of truth for project scope
2. `productContext.md` — Why this project exists, problems it solves, UX goals
3. `activeContext.md` — Current work focus, recent changes, next steps
4. `systemPatterns.md` — Architecture, key technical decisions, design patterns
5. `techContext.md` — Technologies, setup, constraints, dependencies
6. `progress.md` — Module semaphores (✅🔄⏳❌⬜) + plan pointers. Max 60 lines.
7. `plans-index.md` *(volatile, required)* — Index of all active/completed plans with status

### Distribución Volatile / Stable

**🔴 Volátiles — leer SIEMPRE al inicio (máx 60 líneas c/u):**
- `memory-bank/activeContext.md` — snapshot de sesión activa
- `memory-bank/progress.md` — semáforos de módulos
- `memory-bank/plans-index.md` — índice de planes con estado

**🟢 Estables — leer solo bajo demanda:**
- `memory-bank/projectbrief.md` — visión y scope
- `memory-bank/productContext.md` — UX y objetivos
- `memory-bank/systemPatterns.md` — arquitectura y patrones
- `memory-bank/techContext.md` — stack y dependencias

### Loading Protocol

**LEVEL 1 — FAST LOAD (always, every session):**
Read ONLY volatile files:
1. `memory-bank/activeContext.md`
2. `memory-bank/progress.md`
3. `memory-bank/plans-index.md`

**LEVEL 2 — FULL LOAD (on demand):**
Only if user asks about architecture, stack, or goals:
4. `memory-bank/projectbrief.md`
5. `memory-bank/productContext.md`
6. `memory-bank/techContext.md`
7. `memory-bank/systemPatterns.md`

**LEVEL 3 — PLAN LOAD (before executing a task):**
Consult `plans-index.md` → open the specific plan file.

### Additional Context
Create additional files/folders within `memory-bank/` when they help organize complex feature docs, API docs, testing strategies, etc.

## Core Workflows

### Plan Mode
```mermaid
flowchart TD
    Start[Start] --> ReadFiles[Read Memory Bank]
    ReadFiles --> CheckFiles{Files Complete?}
    CheckFiles -->|No| Plan[Create Plan]
    Plan --> Document[Document in Chat]
    CheckFiles -->|Yes| Verify[Verify Context]
    Verify --> Strategy[Develop Strategy]
    Strategy --> Present[Present Approach]
```

### Act Mode
```mermaid
flowchart TD
    Start[Start] --> Context[Check Memory Bank]
    Context --> Update[Update Documentation]
    Update --> Execute[Execute Task]
    Execute --> Document[Document Changes]
```

## Documentation Updates

Memory Bank updates occur when:
1. Discovering new project patterns
2. After implementing significant changes
3. When user requests **update memory bank**
4. When context needs clarification

### Update Protocol (3 steps)

**STEP 1 — VOLATILE (always):**
- `activeContext.md` → update snapshot: branch, next step, blockers, session summary
- `progress.md` → update semaphores if any module changed
- `plans-index.md` → update if a plan was created, completed, or changed status

**STEP 2 — STABLE (only if applicable):**
- `systemPatterns.md` → if architecture or key pattern changed
- `techContext.md` → if a dependency or key version changed

**STEP 3 — Portability:**
The memory-bank in git is the portable source of truth.
Local AI memory/context is a convenience cache — lost when the session ends.

Note: When triggered by **update memory bank**, apply the 3-step Update Protocol above. Focus particularly on `activeContext.md`, `progress.md` and `plans-index.md`.

REMEMBER: After every session reset, I begin completely fresh. The Memory Bank is my only link to previous work. It must be maintained with precision and clarity — my effectiveness depends entirely on its accuracy.

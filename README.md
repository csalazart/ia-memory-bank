# Memory Bank Multiplataforma

## ¿Qué es este repositorio?
Este repositorio reúne plantillas e instrucciones para inicializar un **Memory Bank** coherente en distintos asistentes de IA/IDE (Windsurf, Gemini CLI, Cline, RooCode, Cursor, etc.). El objetivo es copiar la carpeta correspondiente en cada proyecto, ejecutar el comando de inicialización indicado y trabajar con un set uniforme de reglas y contexto persistente.

## Contenido por carpeta
| Carpeta | Asistente / IDE | Archivos clave | Pasos básicos |
| --- | --- | --- | --- |
| `windsurf/` | Editor Windsurf | `.windsurf/rules/core.md`, `.windsurf/rules/memory-bank.md`, `README.md` | Copiar `.windsurf/` al proyecto, abrir el chat e introducir `init memory`. |
| `claude/` | Claude Code | `.claude/CLAUDE.md`, `.claude/settings.json`, `README.md` | Copiar `.claude/` al proyecto, abrir Claude Code e introducir `init memory`. |
| `gemini/` | Gemini CLI | `.gemini/GEMINI.md`, `.gemini/settings.json`, `load-memory.toml`, `README.md` | Copiar `.gemini/` al proyecto y ejecutar `/load-memory` o indicar que lea `GEMINI.md`. |
| `cline/` | Extensión Cline (VS Code) | `memory-bank.md`, `README.md` | Copiar las instrucciones de `memory-bank.md` en las custom instructions o `.clinerules` y pedir "initialize memory bank". |
| `RooCode/` | Extensión RooCode (VS Code) | `.roo/`, `README.md` | Copiar la carpeta `.roo/`, instalar la extensión y en el chat ejecutar `init memory`. |
| `cursor/` | Cursor IDE | `.cursor/`, `README.md` | Copiar `.cursor/` al proyecto, abrir el chat y ejecutar `init memory`. |
| `_templates/` | Todos los asistentes | `activeContext.md`, `progress.md`, `plans-index.md` | Copiar los 3 archivos a `memory-bank/` del proyecto como punto de partida volátil. |

## Flujo general de uso
1. **Clona o descarga** este repositorio junto con tu proyecto.
2. **Elige la carpeta** que corresponde al asistente/IDE con el que vayas a trabajar.
3. **Copia la carpeta oculta** (`.windsurf`, `.roo`, `.cursor`, `.gemini`, etc.) al directorio raíz del proyecto que quieres documentar.
4. **Sigue las instrucciones del README local** (por ejemplo, ejecutar `init memory` o `/load-memory`).
5. **Mantén sincronizados** los archivos del Memory Bank con el proyecto real: actualiza las secciones obligatorias antes de cada sesión y registra cambios relevantes.

## Estructura mínima del Memory Bank
Todos los asistentes comparten el mismo esquema. Los archivos se dividen en dos categorías:

**🔴 Archivos VOLÁTILES — leer SIEMPRE al inicio (máx 60 líneas c/u):**
- `activeContext.md` — snapshot: rama activa, siguiente paso, bloqueantes, resumen última sesión.
- `progress.md` — semáforos de módulos (✅🔄⏳❌⬜) + punteros a planes. Sin detalle inline.
- `plans-index.md` — índice de todos los planes con estado y referencia al fichero.

**🟢 Archivos ESTABLES — leer solo bajo demanda:**
- `projectbrief.md` — visión de alto nivel y metas.
- `productContext.md` — propósito del producto, problemas a resolver y UX deseada.
- `systemPatterns.md` — arquitectura, patrones y dependencias críticas.
- `techContext.md` — stack tecnológico, tooling y restricciones.

Se pueden añadir archivos adicionales (API docs, estrategias de testing, etc.) dentro de `memory-bank/` según lo requiera el proyecto.

## Modos de trabajo y disciplina
Todos los asistentes operan en **3 modos**:

1. **PLAN** (por defecto) - Analizar, diseñar y validar estrategias sin hacer cambios
2. **ACT** - Ejecutar cambios aprobados (activar escribiendo "ACT")
3. **TUTOR** - Modo educativo paso a paso (activar escribiendo "TUTOR:" en el prompt)

Antes de actuar se debe:
1. **Carga rápida** — leer los 3 archivos volátiles:
   `activeContext.md` + `progress.md` + `plans-index.md` (~150 líneas, siempre)
2. **Carga completa** (solo bajo demanda) — si el usuario pregunta sobre arquitectura o stack:
   `projectbrief.md` + `productContext.md` + `techContext.md` + `systemPatterns.md`
3. **Carga de plan** — abrir el plan específico desde `plans-index.md` antes de ejecutar.
4. Elaborar un plan y conseguir la aprobación del usuario.
5. Al terminar: actualizar **siempre** `activeContext.md` + `progress.md` + `plans-index.md`.

Esta disciplina garantiza trazabilidad y evita pérdida de contexto cuando el asistente "reinicia" su memoria entre sesiones.

## Estado actual y siguientes pasos
- Este repositorio solo contiene las **plantillas** y reglas; los archivos `projectbrief.md`, `productContext.md`, etc. deben generarse dentro de cada proyecto que utilice el Memory Bank.
- Mantén este README como referencia rápida y añade secciones nuevas si incorporas más asistentes o procesos.

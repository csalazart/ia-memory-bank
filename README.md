# Memory Bank Multiplataforma

## ¿Qué es este repositorio?
Este repositorio reúne plantillas e instrucciones para inicializar un **Memory Bank** coherente en distintos asistentes de IA/IDE (Windsurf, Gemini CLI, Cline, RooCode, Cursor, etc.). El objetivo es copiar la carpeta correspondiente en cada proyecto, ejecutar el comando de inicialización indicado y trabajar con un set uniforme de reglas y contexto persistente.

## Contenido por carpeta
| Carpeta | Asistente / IDE | Archivos clave | Pasos básicos |
| --- | --- | --- | --- |
| `windsurf/` | Editor Windsurf | `.windsurf/rules/core.md`, `.windsurf/rules/memory-bank.md`, `README.md` | Copiar `.windsurf/` al proyecto, abrir el chat e introducir `init memory`. |
| `gemini/` | Gemini CLI | `memory-bank.md`, `load-memory.toml`, `init-load-memory-command.toml`, `README.md` | Copiar `memory-bank.md` + el comando deseado (local o global) y ejecutar `/load-memory` o indicar en `GEMINI.md` que lea el Memory Bank. |
| `cline/` | Extensión Cline (VS Code) | `memory-bank.md`, `README.md` | Copiar las instrucciones de `memory-bank.md` en las custom instructions o `.clinerules` y pedir “initialize memory bank”. |
| `RooCode/` | Extensión RooCode (VS Code) | `.roo/`, `README.md` | Copiar la carpeta `.roo/`, instalar la extensión y en el chat ejecutar `init memory`. |
| `cursor/` | Cursor IDE | `.cursor/`, `README.md` | Copiar `.cursor/` al proyecto, abrir el chat y ejecutar `init memory`. |
| `.windsurf/` (raíz) | Motor común | Reglas core y workflows aplicados por defecto al proyecto | Se mantiene en el repositorio raíz como referencia y puede reutilizarse si se desea configurar Windsurf directamente desde aquí. |

## Flujo general de uso
1. **Clona o descarga** este repositorio junto con tu proyecto.
2. **Elige la carpeta** que corresponde al asistente/IDE con el que vayas a trabajar.
3. **Copia la carpeta oculta** (`.windsurf`, `.roo`, `.cursor`, `.gemini`, etc.) al directorio raíz del proyecto que quieres documentar.
4. **Sigue las instrucciones del README local** (por ejemplo, ejecutar `init memory` o `/load-memory`).
5. **Mantén sincronizados** los archivos del Memory Bank con el proyecto real: actualiza las secciones obligatorias antes de cada sesión y registra cambios relevantes.

## Estructura mínima del Memory Bank
Todos los asistentes comparten el mismo esquema de archivos, descrito en los `memory-bank.md` específicos:
- `projectbrief.md`: visión de alto nivel y metas.
- `productContext.md`: propósito del producto, problemas a resolver y UX deseada.
- `activeContext.md`: enfoque actual, decisiones recientes y siguientes pasos.
- `systemPatterns.md`: arquitectura, patrones y dependencias críticas.
- `techContext.md`: stack tecnológico, tooling y restricciones.
- `progress.md`: estado actual, pendientes y problemas conocidos.

Se pueden añadir archivos adicionales (API docs, estrategias de testing, etc.) dentro de `memory-bank/` según lo requiera el proyecto.

## Modos de trabajo y disciplina
Las reglas base imponen dos modos: **Plan** (analizar, diseñar y validar estrategias) y **Act** (ejecutar cambios). Antes de actuar se debe:
1. Leer todos los archivos de `memory-bank/`.
2. Elaborar un plan y conseguir la aprobación.
3. Documentar los cambios y actualizar la memoria después de cada iteración.

Esta disciplina garantiza trazabilidad y evita pérdida de contexto cuando el asistente “reinicia” su memoria entre sesiones.

## Estado actual y siguientes pasos
- Este repositorio solo contiene las **plantillas** y reglas; los archivos `projectbrief.md`, `productContext.md`, etc. deben generarse dentro de cada proyecto que utilice el Memory Bank.
- Mantén este README como referencia rápida y añade secciones nuevas si incorporas más asistentes o procesos.

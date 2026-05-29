# Instructions - Generic AI Assistants

Para IAs que usan `AGENTS.md` como estándar de configuración: Qwen, Kimi, ChatGPT, Mistral, DeepSeek, Llama, y cualquier otro asistente sin carpeta de configuración propia.

## Configuración rápida

1. **Copiar `AGENTS.md`** a la raíz de tu proyecto
2. **Copiar `memory-bank.md`** a la raíz de tu proyecto
3. **En el chat**, escribir: `Read AGENTS.md and memory-bank.md, then initialize memory bank`
4. **¡Listo!** La IA seguirá el protocolo para esa sesión

## ¿Qué hace esto?

La carpeta `others/` contiene:
- **AGENTS.md** — Reglas de comportamiento, modos Plan/Act/Tutor y convenciones (equivalente a `CLAUDE.md` / `GEMINI.md`)
- **memory-bank.md** — Protocolo de Memory Bank: distribución Volatile/Stable, carga 3 niveles y update 3 pasos
- **commands/load-memory.md** — Instrucciones del comando `load memory bank`
- **commands/update-memory.md** — Instrucciones del comando `update memory bank`

## Modos de operación

- **PLAN** (por defecto) — La IA genera un plan antes de ejecutar cualquier cambio
- **ACT** — Ejecuta el plan aprobado (escribe "ACT" para activar)
- **TUTOR** — Modo educativo paso a paso (escribe "TUTOR:" en el prompt)

## Comandos disponibles

- **`initialize memory bank`** — Primera inicialización: crea el memory-bank y los 7 archivos base
- **`load memory bank`** — Lee los archivos volátiles e informa del estado actual del proyecto
- **`update memory bank`** — Actualiza el memory-bank al finalizar sesión (activa el Update Protocol)

## Diferencia con Claude y Gemini

| | Claude / Gemini | Others (Qwen, Kimi…) |
|---|---|---|
| Archivo de config | `CLAUDE.md` / `GEMINI.md` | **`AGENTS.md`** (estándar genérico) |
| Carpeta oculta | `.claude/` / `.gemini/` | Ninguna — archivos en la raíz |
| Activación de reglas | Automática al arrancar | Manual: decirle a la IA que lea `AGENTS.md` |
| Comandos | Slash commands `/load-memory` | Frases en el chat |
| Persistencia contexto | Git memory-bank | Git memory-bank |

## Documentación completa

Ver `AGENTS.md` para:
- Comportamiento como compañero de trabajo
- Trigger phrases disponibles
- Reglas críticas y modos de operación

Ver `memory-bank.md` para:
- Estructura completa del memory-bank
- Protocolo de carga y actualización detallado

## Más información

- [Memory Bank Multiplataforma](../README.md) — Guía general del repositorio
- [Claude](../claude/) — Para Claude Code (slash commands, `.claude/`)
- [Gemini](../gemini/) — Para Gemini CLI (slash commands, `.gemini/`)
- [Cline](../cline/) — Para Cline en VS Code

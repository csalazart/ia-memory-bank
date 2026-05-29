# Instructions - RooCode (VS Code)

## Configuración rápida

1. **Instalar la extensión RooCode** en VS Code
2. **Copiar carpeta `.roo`** en la raíz de tu proyecto
3. **En el chat de RooCode**, escribir: `init memory`
4. **¡Listo!** RooCode cargará automáticamente las reglas y memory-bank

## ¿Qué hace esto?

La carpeta `.roo/` contiene:
- **rules-code/rules.md** - Reglas para el modo Code: protocolo de carga 3 niveles, triggers de update y formato por archivo
- **rules-architect/rules.md** - Reglas para el modo Architect: ídem, con enfoque en decisiones de arquitectura
- **mcp.json** - Configuración de MCP servers

Ambos modos usan el mismo protocolo de Memory Bank y distribución Volatile/Stable.

## Modos de operación

- **PLAN** (por defecto) - RooCode genera un plan antes de ejecutar cualquier cambio
- **ACT** - Ejecuta el plan aprobado (escribe "ACT" para activar)
- **TUTOR** - Modo educativo paso a paso (escribe "TUTOR:" en el prompt)

## Documentación completa

Ver `.roo/rules-code/rules.md` para:
- Protocolo de inicialización y carga del memory-bank
- Sección `memory_bank_updates` con triggers y formatos por archivo
- Comando UMB (Update Memory Bank) y sus acciones
- Integración con distribución Volatile/Stable

## Más información

- [Memory Bank Multiplataforma](../README.md) - Guía general del repositorio
- [Claude](../claude/) - Alternativa para Claude Code
- [Cline](../cline/) - Alternativa para Cline
- [Cursor](../cursor/) - Alternativa para Cursor IDE

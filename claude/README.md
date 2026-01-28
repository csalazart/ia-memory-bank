# Instructions - Claude Code

## Configuración rápida

1. **Copiar carpeta `.claude`** en la raíz de tu proyecto
2. **Abrir Claude Code** en tu IDE (VS Code, JetBrains, etc.)
3. **En el chat de Claude**, escribir: `init memory`
4. **¡Listo!** Claude cargará automáticamente las reglas y memory-bank

## ¿Qué hace esto?

La carpeta `.claude/` contiene:
- **CLAUDE.md** - Reglas de comportamiento, modos Plan/Act/Tutor, MCP servers y convenciones
- **settings.json** - Configuración de MCP servers (context7, nuxt, nuxt-ui, postgres) y hooks de seguridad
- **agents/** - Subagentes especializados (opcional, para proyectos complejos)
- **skills/** - Skills reutilizables (opcional)
- **commands/** - Slash commands personalizados (opcional)

## Modos de operación

- **PLAN** (por defecto) - Claude genera un plan antes de ejecutar
- **ACT** - Ejecuta el plan aprobado (escribe "ACT" para activar)
- **TUTOR** - Modo educativo paso a paso (escribe "TUTOR:" en el prompt)

## Documentación completa

Ver `CLAUDE.md` en la carpeta `.claude/` para:
- Comportamiento como compañero de trabajo
- Integración con Memory-Bank
- Uso de MCP servers (documentación oficial)
- Convenciones del proyecto
- Reglas críticas

## Más información

- [Memory Bank Multiplataforma](../README.md) - Guía general del repositorio
- [Cline](../cline/) - Alternativa para VS Code
- [Windsurf](../windsurf/) - Alternativa para Windsurf IDE

# Instructions - Devin IDE

## Configuración rápida

1. **Copiar carpeta `.devin`** en la raíz de tu proyecto
2. **Abrir Devin IDE**
3. **En el chat de Devin**, escribir: `init memory`
4. **¡Listo!** Devin cargará automáticamente las reglas y memory-bank

## ¿Qué hace esto?

La carpeta `.devin/` contiene:
- **rules/memory-bank.md** - Protocolo de Memory Bank: modos Plan/Act/Tutor, distribución Volatile/Stable, carga 3 niveles y update 3 pasos
- **rules/core.md** - Reglas generales de comportamiento, convenciones y estilo del proyecto

## Modos de operación

- **PLAN** (por defecto) - Devin genera un plan antes de ejecutar cualquier cambio
- **ACT** - Ejecuta el plan aprobado (escribe "ACT" para activar)
- **TUTOR** - Modo educativo paso a paso (escribe "TUTOR:" en el prompt)

## Documentación completa

Ver `rules/memory-bank.md` en la carpeta `.devin/` para:
- Comportamiento como compañero de trabajo
- Integración con Memory-Bank y distribución Volatile/Stable
- Workflows Plan/Act con diagramas
- Project Intelligence (projectRules.md)
- Protocolo de carga y actualización detallado

## Más información

- [Memory Bank Multiplataforma](../README.md) - Guía general del repositorio
- [Claude](../claude/) - Alternativa para Claude Code
- [Gemini](../gemini/) - Alternativa para Gemini CLI
- [Cline](../cline/) - Alternativa para VS Code

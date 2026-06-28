# Instructions - Cursor IDE

## Configuración rápida

1. **Copiar carpeta `.cursor`** en la raíz de tu proyecto
2. **Abrir Cursor IDE**
3. **En el chat de Cursor**, escribir: `init memory`
4. **¡Listo!** Cursor cargará automáticamente las reglas y memory-bank

## ¿Qué hace esto?

La carpeta `.cursor/` contiene:
- **rules/memory-bank.mdc** - Protocolo de Memory Bank: modos Plan/Act/Tutor, distribución Volatile/Stable, carga 3 niveles y update 3 pasos
- **rules/core.mdc** - Reglas generales de comportamiento, convenciones y estilo del proyecto

Los archivos `.mdc` se activan automáticamente en cada sesión de Cursor.

## Modos de operación

- **PLAN** (por defecto) - Cursor genera un plan antes de ejecutar cualquier cambio
- **ACT** - Ejecuta el plan aprobado (escribe "ACT" para activar)
- **TUTOR** - Modo educativo paso a paso (escribe "TUTOR:" en el prompt)

## Documentación completa

Ver `rules/memory-bank.mdc` en la carpeta `.cursor/` para:
- Comportamiento como compañero de trabajo
- Integración con Memory-Bank y distribución Volatile/Stable
- Convenciones del proyecto y reglas críticas



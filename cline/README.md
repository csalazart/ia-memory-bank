# Instructions - Cline (VS Code)

## Configuración rápida

1. **Instalar la extensión Cline** en VS Code
2. **Copiar `memory-bank.md`** al proyecto como `.clinerules` o pegar su contenido en las Custom Instructions de Cline
3. **En el chat de Cline**, escribir: `initialize memory bank`
4. **¡Listo!** Cline cargará automáticamente las reglas y memory-bank

## ¿Qué hace esto?

El archivo `memory-bank.md` contiene:
- **Reglas de comportamiento** - Modos Plan/Act/Tutor, estilo y convenciones del proyecto
- **Distribución Volatile/Stable** - 🔴 3 archivos volátiles (leer siempre) + 🟢 4 archivos estables (bajo demanda)
- **Protocolo de carga** - 3 niveles para cargar el memory-bank eficientemente cada sesión
- **Protocolo de update** - 3 pasos para actualizar el memory-bank al finalizar sesión
- **Inicialización** - Instrucciones para crear el memory-bank desde cero en proyectos nuevos

## Comandos disponibles

- **`initialize memory bank`** — Primera inicialización: crea el memory-bank y los 7 archivos base
- **`update memory bank`** — Actualiza el memory-bank al finalizar sesión (activa el Update Protocol)

## Modos de operación

- **PLAN** (por defecto) - Cline genera un plan antes de ejecutar cualquier cambio
- **ACT** - Ejecuta el plan aprobado (escribe "ACT" para activar)
- **TUTOR** - Modo educativo paso a paso (escribe "TUTOR:" en el prompt)

## Documentación completa

Ver `memory-bank.md` para:
- Comportamiento completo como compañero de trabajo
- Integración con Memory-Bank (estructura, carga y update)
- Convenciones del proyecto y reglas críticas

## Más información

- [Memory Bank Multiplataforma](../README.md) - Guía general del repositorio
- [Claude](../claude/) - Alternativa para Claude Code
- [Windsurf](../windsurf/) - Alternativa para Windsurf IDE
- [RooCode](../RooCode/) - Alternativa para RooCode

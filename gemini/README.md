# Instructions - Gemini CLI

## Configuración rápida

1. **Copiar carpeta `.gemini`** en la raíz de tu proyecto
2. **Abrir Gemini CLI** en tu terminal
3. **En Gemini**, escribir: `/load-memory` o indicar que lea `GEMINI.md`
4. **¡Listo!** Gemini cargará automáticamente las reglas y memory-bank

## ¿Qué hace esto?

La carpeta `.gemini/` contiene:
- **GEMINI.md** - Reglas de comportamiento, modos Plan/Act/Tutor, MCP servers y convenciones
- **settings.json** - Configuración de MCP servers (context7, nuxt) y preferencias globales
- **commands/** - Slash commands personalizados (opcional)

## Modos de operación

- **PLAN** (por defecto) - Gemini genera un plan antes de ejecutar
- **ACT** - Ejecuta el plan aprobado (escribe "ACT" para activar)
- **TUTOR** - Modo educativo paso a paso (escribe "TUTOR:" en el prompt)

## Opciones de instalación

### Opción 1: LOCAL PROJECT (Recomendado)
1. Copiar la carpeta `.gemini/` al proyecto
2. Inicializar Gemini: `gemini init`
3. Gemini cargará automáticamente `GEMINI.md` como contexto global

### Opción 2: LOCAL WITH COMMANDS
1. Crear/abrir `.gemini/commands/` en el proyecto
2. Copiar archivos `.toml` (load-memory.toml, etc.)
3. Ejecutar `/load-memory` en Gemini para cargar memory-bank

### Opción 3: GLOBAL (Todos los proyectos)
1. Ir a carpeta global:
   - **Windows:** `c:\users\USUARIO\.gemini`
   - **Linux/Mac:** `~/.gemini`
2. Copiar `GEMINI.md` en esa carpeta
3. Gemini leerá automáticamente el archivo en cada sesión

## Archivos incluidos

- **GEMINI.md** - Configuración principal y reglas de comportamiento
- **settings.json** - MCP servers y configuración de IDE
- **load-memory.toml** - Comando para cargar memory-bank (opcional)
- **init-load-memory-command.toml** - Comando de inicialización (opcional)
- **memory-bank.md** - Documentación del Memory Bank (ver archivo separado)

## Documentación completa

Ver `GEMINI.md` en la carpeta `.gemini/` para:
- Comportamiento como compañero de trabajo
- Integración con Memory-Bank
- Uso de MCP servers (documentación oficial)
- Convenciones del proyecto
- Reglas críticas

## Más información

- [Memory Bank Multiplataforma](../README.md) - Guía general del repositorio
- [Claude](../claude/) - Alternativa para Claude Code
- [Windsurf](../windsurf/) - Alternativa para Windsurf IDE
- [Cline](../cline/) - Alternativa para VS Code

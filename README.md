# Claude Code Plugins

Colección de plugins para Claude Code.

## Plugins Disponibles

### conversation-logger

Plugin que registra automáticamente las conversaciones en archivos de log locales con rotación automática.

**Características:**
- Captura mensajes del usuario, uso de herramientas y respuestas del asistente
- Logs en `.claude/logs/` con rotación automática (512 KB)
- Solo Windows (PowerShell 5.1+)

```bash
/plugin enable conversation-logger@practia-ia
```

### useful-commands

Plugin con comandos útiles para gestión de PRs y documentación de sesiones.

**Comandos incluidos:**

| Comando | Descripción |
|---------|-------------|
| `/create-pr` | Crea un PR en Azure DevOps |
| `/update-pr` | Actualiza un PR existente en Azure DevOps |
| `/create-pr-gh` | Crea un PR en GitHub |
| `/update-pr-gh` | Actualiza un PR existente en GitHub |
| `/adr` | Crea un Architecture Decision Record |
| `/document` | Documenta la sesión actual |

**MCP Servers incluidos:**
- [Microsoft Azure DevOps MCP](https://github.com/microsoft/azure-devops-mcp)
- [GitHub MCP Server](https://github.com/github/github-mcp-server)

```bash
/plugin enable useful-commands@practia-ia
```

## Instalación

```bash
# Registrar el marketplace
/plugin marketplace add practia-ia/claude_code_plugins

# Habilitar los plugins que desees
/plugin enable conversation-logger@practia-ia
/plugin enable useful-commands@practia-ia
```

## Requisitos

- **Claude Code** versión 1.0.40+ (soporte de plugins)
- **Node.js 20+** (para Azure DevOps MCP)
- **Docker** (para GitHub MCP)
- **Windows con PowerShell 5.1+** (solo para conversation-logger)

## Licencia

MIT

## Autor

practiauy

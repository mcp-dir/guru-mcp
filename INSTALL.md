# Instalação rápida

Digital Manager Guru é um servidor MCP remoto hospedado em `https://api.mcp.ai/p_guru`. Você não baixa nem roda nada localmente — só aponta seu cliente pra essa URL.

A auth acontece em runtime: clientes com **OAuth 2.1** (Claude Desktop, Cursor, VS Code recentes) abrem o browser na 1ª chamada (magic-link). Clientes sem OAuth recebem a tool `authenticate` — abra `https://app.mcp.ai/agent-auth`, faça login, copie o JWT e cole no chat.

---

## Claude (Web e Desktop)

[➕ Abrir no Claude e conectar](https://claude.ai/new?modal=add-custom-connector#settings/customize-connectors)

Manual: [claude.ai/customize/connectors](https://claude.ai/customize/connectors?surface=cowork) → **+** → **Adicionar conector personalizado** → `Digital Manager Guru` / `https://api.mcp.ai/p_guru`.

Config file (legado): `~/Library/Application Support/Claude/claude_desktop_config.json` (macOS) ou `%APPDATA%\Claude\claude_desktop_config.json` (Windows):

```json
{ "mcpServers": { "guru": { "type": "http", "url": "https://api.mcp.ai/p_guru" } } }
```

## Cursor

[➕ Instalar no Cursor](cursor://anysphere.cursor-deeplink/mcp/install?name=guru&config=eyJ1cmwiOiJodHRwczovL2FwaS5tY3AuYWkvcF9ndXJ1In0=)

`.cursor/mcp.json`:
```json
{ "mcpServers": { "guru": { "url": "https://api.mcp.ai/p_guru" } } }
```

## VS Code (Copilot Chat)

[➕ Instalar no VS Code](vscode:mcp/install?name=guru&config=%7B%22type%22%3A%22http%22%2C%22url%22%3A%22https%3A%2F%2Fapi.mcp.ai%2Fp_guru%22%7D)

`.vscode/mcp.json`:
```json
{ "servers": { "guru": { "type": "http", "url": "https://api.mcp.ai/p_guru" } } }
```

## Outros clientes MCP

Qualquer cliente com **MCP over HTTP**. URL fixa:

```
https://api.mcp.ai/p_guru
```

Dúvidas? [guru@mcp.ai](mailto:guru@mcp.ai)

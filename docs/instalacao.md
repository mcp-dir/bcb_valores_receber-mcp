# Instalação detalhada

Banco Central do Brasil (BCB): Valores a Receber é um servidor MCP remoto. Aponte seu cliente pra `https://api.mcp.ai/p_bcb_valores_receber`. Snippets rápidos: [INSTALL.md](../INSTALL.md).

| Cliente | URL | Auth |
|---|---|---|
| Claude Desktop | `https://api.mcp.ai/p_bcb_valores_receber` | OAuth 2.1 ou agent-auth |
| Cursor | `https://api.mcp.ai/p_bcb_valores_receber` | OAuth 2.1 ou agent-auth |
| VS Code (Copilot) | `https://api.mcp.ai/p_bcb_valores_receber` | OAuth 2.1 ou agent-auth |

A config JSON é a mesma em todos: só a URL, sem headers.

## Desinstalar

Remova o bloco `mcpServers.bcb_valores_receber` (ou `servers.bcb_valores_receber` no VS Code) do config do cliente e reinicie.
